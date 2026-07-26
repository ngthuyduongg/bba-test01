# Javascript Basic (Continue)

## Phạm vi của biến (Scope)

Xác định nơi mà biến có thể truy cập.

**Block Scope** - phạm vi trong `if`, `for`, `while` hoặc `{}`
- `let`, `const`: chỉ dùng được trong khối `{}` đó
- `var`: không bị giới hạn bởi block

**Function Scope** - phạm vi bên trong function
- Các biến khai báo trong function chỉ dùng được trong function đó

**Global Scope** - phạm vi ngoài mọi function và mọi khối `{}`
- Có thể dùng được ở bên ngoài và trong các scope bên trong

---

## Break & Continue (trong vòng lặp)

**break**
- Dừng toàn bộ vòng lặp ngay lập tức
- Dùng khi đã đạt điều kiện cần và không cần lặp tiếp (ví dụ: tìm thấy phần tử cần tìm)
- Kết quả: vòng lặp dừng luôn

**continue**
- Bỏ qua lần lặp hiện tại, sang lần lặp tiếp theo
- Dùng khi muốn bỏ qua một số trường hợp nhưng vẫn tiếp tục lặp (ví dụ: lọc dữ liệu)
- Kết quả: vòng lặp vẫn tiếp tục

---

## Câu điều kiện nâng cao

**if...else** - dùng khi chỉ có 2 trường hợp: đúng / sai
- Đúng → chạy `if`; sai → chạy `else`

**if...else if...else** - dùng khi cần kiểm tra nhiều mức điều kiện, theo thứ tự
- Kiểm tra từ trên xuống, đúng cái nào dừng cái đó, không xét tiếp

**Ternary (`? :`)** - dùng khi muốn viết gọn thay cho if...else đơn giản
- Cú pháp: `điều_kiện ? giá_trị_true : giá_trị_false`
- Có thể lồng nhiều tầng nhưng dễ rối, khó đọc

---

## Vòng lặp nâng cao

**for...in (với Object)**
- Dùng để duyệt qua các key/property của Object (Object không có index như Array)
- Cú pháp: `for (let key in object)` → lấy giá trị bằng `object[key]`
- Lưu ý: `key` là tên thuộc tính

**for...in (với Array)**
- Dùng để duyệt qua các index của Array
- Không khuyến khích dùng cho Array
- Cú pháp: `for (let index in array)` → lấy giá trị bằng `array[index]`
- Lưu ý: `index` thường là chuỗi: "0", "1", "2"

**forEach Method**
- Dùng để thực hiện một function cho từng phần tử trong Array
- Dùng khi cần xử lý từng phần tử và không cần `break`/`continue`
- Cú pháp: `array.forEach(function(value) { ... })`
- Lưu ý: không dùng được `break` / `continue`

---

## Utils Function

Là các hàm có sẵn của Javascript, giúp việc code trở nên nhanh hơn, gọn hơn.

### String Utils

- `trim()` - xóa khoảng trắng đầu và cuối chuỗi
- `trimStart()` / `trimEnd()` - xóa khoảng trắng đầu / cuối chuỗi
- `toUpperCase()` / `toLowerCase()` - chuyển chuỗi thành chữ hoa / chữ thường
- `includes()` - kiểm tra chuỗi có chứa chuỗi con hay không, trả về true/false
- `split(<ký_tự_tách>)` - tách chuỗi thành mảng tại vị trí ký tự tách
- `replace()` - thay thế chuỗi con (chỉ lần đầu tiên); `replaceAll()` - thay thế tất cả

### Array Utils

- `push()` / `unshift()` - thêm phần tử vào cuối / đầu mảng
- `pop()` / `shift()` - xóa phần tử ở cuối / đầu mảng
- `splice(vị_trí, số_lượng, phần_tử_thêm)` - thêm hoặc xóa phần tử ở vị trí bất kỳ
- `find(điều_kiện)` - trả về phần tử đầu tiên thỏa điều kiện, hoặc `undefined` nếu không có
- `filter(điều_kiện)` - trả về mảng gồm tất cả phần tử thỏa điều kiện
- `map(hàm_xử_lý)` - tạo mảng mới bằng cách áp dụng hàm lên từng phần tử
- `sort((a, b) => a - b)` - sắp xếp tăng dần; `sort((a, b) => b - a)` - sắp xếp giảm dần