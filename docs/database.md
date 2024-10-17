
<h1 align="center">
  <br>
  데이터베이스
  <br>
</h1>
<p align="center">
  서버 데이터베이스 관련 문서
</p>

## Schema
총 3개의 테이블로 이루어져 있습니다.
- wifiinfo : WiFi 신호의 스캔 데이터들을 모아둔 테이블
```json
{
  "id": "unsigned int",
  "pos_x": "float",
  "pos_y": "float",
  "SSID": "String",
  "BSSID": "String",
  "frequency": "int",
  "level": "int",
  "building": "String",
  "date": "Date",
  "uuid": "String",
  "method": "String"
}
```
- fingerprint : Fingerprint 기반의 실내측위 결과를 담아둔 테이블
```json
{
  "id": "unsigned int",
  "pos_x": "float",
  "pos_y": "float",
  "est_x": "float",
  "est_y": "float",
  "SSID": "String",
  "building": "String",
  "date": "Date",
  "uuid": "String",
  "k": "int",
  "threshold": "int",
  "method": "String",
  "algorithmVersion": "int"
}
```
- barcode : Fingerprint Map의 자동 업데이트를 위해 바코드 정보를 보관하는 테이블
```json
{
  "id": "unsigned int",
  "pos_x": "float",
  "pos_y": "float",
  "barcode_serial": "String",
  "building": "String",
  "date": "Date"
}
```
