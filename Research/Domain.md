# Domain

## Domain là

Domain, hay được gọi là tên miền, là tên được gán cho đia chỉ website.

## Các trạng thái của

### Trạng thái tên miền tại đơn vị Cấp (Registry)

|  Status code | Ý nghĩa |
| :---: | :--- |
| OK/activ | Domain trạng thái thể hiện tên miền hoạt động bình thường |
| addPeroid | Là trạng thái sau khi tên miền vừa mới được đăng ký |
| autoRenewPeroid |Thời gian đăng ký tự động gia hạn tên miền. Trạng thái này cho phép nhà đăng ký hủy việc gia hạn (duy trì) nhưng phải trả một khoản phí cho nhà cung cấp |
| inactive | Tên miền được đăng ký nhưng Name Servẻ chưa thể liên kết với tên miền của bạn |
| pendingCreate | Đang chờ Đăng ký |
| pendingDelete | Tên miền hết hạn đăng ký. Chuẩn bị xóa. |
| pendingRenew | Đang chờ gia hạn |
| pendingRestore | Một tên miền đã hết hạng đang chờ được khôi phục (về trạng thái Active). Nếu trong thời gian này nhà đăng ký không thực hiện yêu cầu khôi phục nào, tên miền sẽ về trạng thời redemptionPeroid. |
| pendingTransfer | Đang chờ Chuyển đổi nhà đăng ký. |
| pendingUpdate | Đang chờ cập nhật |
| redemption Peroid | Tên miền đã hết hạn và rơi vào trạng thái cần đống phí chuộc nếu muốn tiếp tục sử dụng. Thời gian thường sẽ kéo dài 30 ngày |
| renewPeroid | Tên miền được gia hạn |
| serverDeleteProhibited | Trạng thái tên miền bị xóa |
|  serverHold | Tên miền không được kích hoạt trong DNS |
| serverRenewProhibited | Trạng thái không thể được gia hạn. Nó là trạng thái không thông dụng vì nó có hiệu lực trong quá trình tranh chấp pháp lý |
| serverTransferProhibited | Trạng thái không cho phép transfer tên miền. |
| serverUpdateProhibited | Trạng thái không cho phép cập nhật tên miền | 
| transferPeroid | Trạng thái cho phép sau khi tranfer tên miền thành công thì nhà đăng ký mới có thể yêu cầu nhà cung cấp xóa tên miền. |

### Trạng thái tên miền tại đơn vị quản lý tên miền (Registrar)

| Status code | Ý nghĩa |
| :---: | :--- |
| clientDelteProhibited | Trạng thái không cho phép xóa tên miền |
| clientHold | Trạng thái suspend tên miền |
| clientRenewProhibited | Trạng thái khong cho phép gia hạn tên miền |
| clientTransferProhibited | Trạng thái không cho phép transfer tên miền |
| clientUpdateProhibited | Trạng thái không cho phép cập nhật thông tin |

## Subdomain là gì

Subdomain là phần bổ sung xuất hiện trước của tên miền chính. Subdomain là một phần tách ra từ domain và hoạt động như một website bình thường.

## Virtual Hosts là gì

Virtual Hosts là giải pháp cho phép host nhiều domain trên cùng một webserver.
