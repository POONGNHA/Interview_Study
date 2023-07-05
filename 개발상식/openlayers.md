Feature Type ::

- 점(Point)

- 점(Multi Point)

- 선(LineString)

- 다 선(Multi LineString)

- 다각형(Polygon)

- 다 다각형(Multi Polygon)

- 원형(Circle)

Source는 Feature들이 담기는 그릇, Layer는 그릇들을 모은 하나의 그릇보관함이라고 생각

다각형이 그려지면 거기에 label이나 name등 특성들이 들어가는데 그 특성들이 바로 feature라고 생각하면 된다.


## openlayers layer별 오류 해결(23'07'05)
한양대 도시생태계 프로젝트 중에 edit Layer와 vectortile Layer가 서로 겹치는 부분을 intersection하는 기능이 제대로 동작하지 않는다는 것을 발견하였다.
에러의 원인이 처음에는 수원시 전체를 계산한 edit 레이어에 있다고 생각하여 이전에 발생했던 java utf-16 filewrite encode 에러를 참조하였는데, 
edit 레이어는 문제가 없었고, 이 edit Layer와 페이지 로드 할 때마다 발생하는 vectortile Layer를 그리는 작업이 잘못되었다고 발견하였다.
결론부터 말하면 설계 미스였다. 
vectorTile을 shp파일에서 계산할때, 각 feature들의 SGG_oid를 불러와서 그 feature에 intersection 되는 oid를 key값으로 제거하는 것이 기존 코드의 알고리즘이었는데,
큰 영역의 (여러 필지가 합쳐져잇는) shp 파일을 처음부터 불러올때 이미 여러 feature의 SGG_OID를 가져오지 않고 프로그램을 만들어서 intersection이 불가능 한것이었다.
따라서 처음 shp파일의 extent를 계산하여 minx와 miny, maxx와 maxy를 저장하고, edit file에 geojson형식으로 저장하여
페이지를 로드 할때마다 그 extent에 겹치는 SGG_OID를 삭제하는 형식으로 코드를 수정하였다.
