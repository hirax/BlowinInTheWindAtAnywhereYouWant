# BlowinInTheWindAtAnywhereYouWant

Software Design 記事の図２に関しては、下記の修正が必要です。
（一行のスペースを減らそうとしてバグを入れてしまいました）
現在のJupyterコードは修正済みバージョンです。

    def getMapFromOSM(lon,lat, nx, ny):
        angle=0.000001
        map = smopy.Map((lon,lat,lon+angle,lat+angle),z=19)
        mapImg = map.to_numpy()
        return mapImg, cv2.resize(mapImg, (nx, ny))

