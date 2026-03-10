<!DOCTYPE html> báo cho trình duyệt là đang sdung phiên bản HTML mới nhất

<html></html> dùng để định nghĩa phần thân tài liệu HTML , dùng kèm theo field lang để chỉ định ngôn ngữ được viết của web

<head></head> dùng để chứa các thông tin về trang web mà ko đc hiển thị trực tiếp trên trình duyệt của user.

1 : Max <= <h> <= 6: Min

alt + shift + mũi tên xuống

<title></title> Tiêu đề trang web (hiển thị trên tab browser).

<p></p> Chứa đoạn văn bản (paragraph)
<body></body> Chứa nội dung chính để hiển thị trên giao diện web

<hr> : Đường ngang phân cách
<br> Ngắt dòng, xuống dòng (empty).

<b> == <strong>: in đậm
<i> == <em>: in nghiêng
<u> gạch chân

<ul> : dsach ko thứ tự 
<ol> : dsach có thứ tự (stt) 
  -- reversed: đảo ngược, type = "a-z, A-Z,1,."
<li> : thẻ con trực tiếp trong dsach <ul>,<ol>

ul(or ol)>li\*n + {nội dung trong li}

<a></a> : gắn kèm liên kết,email,.. trong field href

- field target = :
  "\_self" -> mở gdiện web phản hồi trong chính tab hiện tại(default)
  "\_blank" -> mở gdiện web phản hồi trong tab mới
  "\_parent" -> Mở trong khung cha (dùng khi có iframe)
  "\_top" -> Mở ở toàn bộ cửa sổ, thoát khỏi mọi iframe

  hoạt động : <a href="https://grok.com/"> grok </a>

1. Bấm vào liên kết "grok"
2. trình duyệt đọc field href
3. gửi request đến địa chỉ đó (https://grok.com/)
4. Nhận phản hồi từ máy chủ grok
5. thay thế trang hiện tại(default) = hiển thị ndung phản hồi trên web

<img src="" alt="" width="" height=""/> : thẻ tự động đóng, dùng để hiển thị hình ảnh trên web

- field src : sdung để chỉ định đường dẫn tới tập tin ảnh

- field alt : Hiển thị text khi link ảnh lỗi .
  Công cụ tìm kiếm thu thập dữ liệu trên trang.

- width : chiều rộng ảnh
- height : chiều cao ảnh

* ./(đường dẫn tương đối) : chỉ tệp, ảnh, thư mục bằng cấp or thư mục con của thư mục bằng cấp.
* ../(đường dẫn tương đối) : chỉ tệp, ảnh cấp trên trước nó.

* / (đường dẫn tuyệt đối) : chỉ thư mục gốc sau đó mới thư mục , ảnh , tệp con .

<pre></pre> : giữ nguyên định dạng văn bản kể cả khoảng trắng dư thừa,..

<code></code>: hiển thị đoạn mã code , kết hợp với <pre> để hiển thị nhiều dòng code

<table></table>: vẽ bảng
<tr></tr>: đại diện cho 1 hàng trong bảng
<td></td>: định nghĩa 1 ô dữ liệu trong bảng
<th></th>: định nghĩa 1 ô tiêu đề

<thead></thead> (table head): Dùng để chứa hàng tiêu đề (header) của bảng.
<tbody></tbody> (table body): Chứa nội dung chính của bảng
<tfoot></tfoot> (table footer):Chứa tổng kết, ghi chú hoặc tổng số ở cuối bảng
 💡Rõ ràng cấu trúc => Phân tách phần đầu, thân, chân giúp dễ đọc và bảo trì

- colspan : chỉ định phần tử chiếm bao nhiêu cột
- rowspan : chỉ định phần tử chiếm bao nhiêu hàng

CSS:

- Inline( CSS nội tuyến) : là cách viết mã CSS ngay bên trong phần tử cơ bản HTML. (cấp cao nhất)

  VD: <h1 style="color: brown">ok</h1>

  - style : thuộc tính (name of Attribute)
  - "..." : giá trị (Value for Attribute)
  - color : property
  - brown(màu tùy chọn) : value

- Internal(css nội bộ): là cách viết mã CSS trong cặp thẻ
<style></style> (đặt trong khối <head></head>)

- External(css bên ngoài): trong trường hợp muốn áp dụng cho all các file html nằm trên trang web, (code 1 lần có thể sử dụng ở nhiều nơi)

   <link rel="stylesheet" href="style.css" />

  -- liên kết (kết nối) file CSS bên ngoài (style.css) với file HTML hiện tại.Mọi qtắc định dạng trong style.css sẽ áp dụng cho HTML.css

💡Giữa Internal và External , thằng nào viết sau => thằng đó được áp dụng (giống như thằng sau ghi đè thằng trước)

<span></span>:dùng để bao quanh 1 phần nhỏ của văn bản hoặc 1 vài phần tử inline khác,
để áp dụng CSS hay thay đổi định dạng cho đúng phần đó

✨<div></div>(thẻ chia khối (block) trong HTML.)
-- dùng để gom nhóm (group) nhiều phần tử HTML lại với nhau, giúp dễ quản lý, dễ trang trí bằng CSS, và dễ bố cục trang web.

- field "opacity"(CSS) : Quy định độ trong suốt
  ❗trong suốt không nhìn thấy vẫn chiếm vị trí vẫn có thể copy
- field "display"(CSS) : Ẩn phần tử khỏi giao diện (xóa cả không gian nó chiếm) (none)
- field "visibility"(CSS) : Ẩn(hidden) hoặc hiện(visible) element
  ❗với hidden : trong suốt không nhìn thấy, vẫn chiếm vị trí và không thể copy

* Favicon (favorite icon) : logo nhỏ đại diện cho 1 trang web

- ID selector(gọi #): Khi chỉ muốn áp dụng CSS cho 1 phần tử
  chỉ định nào đó của HTML -> dùng id(id là duy nhất)

- Class Selector(gọi .): Do không thể sử dụng lại tên id
  -> Trong trường hợp muốn khai báo lặp lại thì dùng class

<block><block> :luôn nằm trên một dòng riêng.Nó đẩy các phần tử khác xuống dòng tiếp theo.

-- '\*selector' - chọn all element(ptu HTML)
-- 'space selector' - chọn all thẻ s2 nằm trong thẻ s1

• div p :Chọn all thẻ <p> nằm bên trong <div>

• div > p:Chỉ chọn các thẻ <p> là con trực tiếp (direct child) của <div>.

• div + p:Chọn ptu <p> đầu tiên ngay sát sau ptu <div>
-- ví dụ: h1 + h2 -> áp dụng css cho thẻ <h2> đứng sát sau <h1>
❗nếu giữa <h1> và <h3> có <h2> thì
-> h1 + h3 sẽ không được áp dụng

• h1 ~ h2 :chọn all các thẻ <h2> cùng cấp và nằm sau <h1>

--Attribute selector

- [Attribute] : chọn all thuộc tính
- [Attribute=value] : chọn all Attribute có chính xác giá trị (vd: [target="_blank"])

- [Attribute~=value] : chọn all các Attribute có chứa value nằm đơn lẻ
  vd: [title~="pic"] -> chọn all title có chứa từ pic trong giá trị: pic aa, pic 123abc,, dhx pic,..

- [Attribute*=value] : Chọn all Attribute có chứa value kể cả có liền với ký tự khác  
  vd: [title*="pic"] -> pic aa, pic12bch, abhcpic, ..

- [Attribute|=value] : chọn all Attribute có gtrị bắt đầu là value
  đứng đơn lẻ hoặc sau value là giá trị khác và phải các nhau bằng dấu "-".
  vd: [title|="pic"] -> pic sdhf, pic-adbdn, ...

- [Attribute^=value] : Chọn all Attribute bắt đầu bằng value không quan tâm cách, liền, dấu gạch.
  vd: [title^="pic"] -> pic cjg, pic-cbsj-chn, pichkfg,..

- [Attribute$=value] : Chọn all Attribute kết thúc bằng value
  vd: [title$="c"] -> abc jg c, qhedc

✨pseudo-classes:
-- :hover (vd: p:hover) : Chọn các thẻ <p> khi `di chuột qua`
-- :active (vd: a:active) : Chọn các thẻ <a> khi `nhấn giữ chuột`
-- :link (vd: a:link) : Chọn các thẻ <a> có liên kết `chưa click vào`
-- :visited (vd: a:visited) : Chọn các thẻ <a> có liên kết `đã click truy cập`
-- :empty (vd: div:empty) : Chọn các thẻ <div> không có nội dung
-- :target (vd: #home:target) : Chọn thẻ có id="home" khi trên URL có hash tương ứng. VD: https://domain.com/#home

-- :first-child (vd: p:first-child) : chọn các thẻ <p> là thẻ con đầu tiên (đk: ko có thẻ nào khác trước nó)

-- :last-child (vd: p:last-child) : chọn các thẻ <p> là thẻ con cuối cùng 

-- :nth-child(n: 1,2,3,...) (vd: p:nth-child(2)): chọn các thẻ <p> là thẻ con thứ 2 từ trên xuống (đk: ko có thẻ nào khác trước nó)

-- :nth-last-child(n) (vd: p:nth-last-child(2)): chọn các thẻ <p> là thẻ con thứ 2 tính từ cuối lên (đk: ko có thẻ nào khác trước nó) 

-- :only-child (vd: only-child): chọn các thẻ <p> là thẻ con duy nhất 

-- :first-of-type (vd: p:first-of-type): chọn các thẻ <p> xuất hiện đầu tiên trong thẻ cha

-- :last-of-type (vd: p:last-of-type): chon các thẻ <p> xuất hiện cuối cùng trong thẻ cha

-- :nth-of-type(n) (vd: p:nth-of-type(2)): chọn các thẻ <p> xuất hiện lần thứ 2 trong thẻ cha tính từ trên xuống

-- :nth-last-of-type(n) (vd: p:nth-last-of-type(2)): chọn các thẻ <p> xuất hiện lần thứ 2 trong thẻ cha tính từ cuối lên

-- :only-of-type (vd: p:only-of-type): chọn các thẻ <p> xuất hiện duy nhất trong thẻ cha

-- :not(selector) (vd: .top:not(p)): Chọn các thẻ có class="top" loại trừ thẻ <p>

🧠Mức độ từ yếu -> mạnh khi áp dụng CSS ghi đè:
" * selector" -> "element selector" -> class -> id -> inline -> !important

✨Box Model: Trình duyệt luôn coi mỗi phần tử là 1 box - hộp chữ nhật

- Nội dung ⊂ padding ⊂ border ⊂ margin:
  + Nội dung(width,height) -> hình ảnh, text, ...

  + padding -> khoảng đệm nội dung và viền(ko chứa nội dung) top,bottom,left,right

  + border(-width,color,style,radius) -> viền của phần tử
   - solid: nét liền
   - dashed: đường nét đứt 
   ...
  + margin -> khoảng cách với các phần tử liền kề khác
     top,bottom,left,right

+ Box-sizing:Content-box -  Áp dụng width/height cho phần content(nội dung) 
 - Padding + Border sẽ cộng thêm vào kích thước thực tế của content.

+ Box-sizing:Border-box - Áp dụng width/height cho all 
  phần tử (gồm: content,padding,border)
  - không làm kích thước phình to ra

  
+ display: block - Chiếm toàn bộ chiều ngang và luôn xuống dòng.
 - đặc điểm: 
    + Luôn bắt đầu trên dòng mới
    + sử dụng được width, height
    + margin, padding hoạt động đầy đủ

+ display: inline - Phần tử nằm cùng dòng, giống chữ trong văn bản.
 - đặc điểm:
    + Không xuống dòng
    + không sdung đc width, height
    + margin-top / margin-bottom không có tác dụng
    + Kích thước phụ thuộc nội dung

+ display: inline-block - Kết hợp ưu điểm của inline + block.
 - đặc điểm: 
    + không xuống dòng
    + sdung đc width,height
    + margin,padding hoạt động đầy đủ


CSS units:
 + "px"(pixel) - tuyệt đối
 + "%"(vd: 50%) ->  kích thước 50% so với phần tử cha (tương đối)
 + "vw"(viewport-width) - (vd: 50vw) -> 50% chiều rộng khung hình 
 + "vh"(viewport-height) - (vd: 20vh) -> 20% chiều cao khung hình 
 + "em"() - (vd: 2em): kích thước gấp 2 lần font chữ hiện tại (có extend)
 + "rem" -(vd: 3rem): kích thước 3 lần font chữ mặc định (ko extends)

default font-size : 16px

-- text-decoration property:
value: 
  + none: bỏ gạch chân
  + underline: thêm gạch chân
  + line-through: thêm gạch ngang
  + overline: gạch trên đầu

-- text-indent:  thụt lề
-- text-transform:
value:
  + capitalize: viết hoa chữ cái đầu
  + lowercase: viết thường all text
  + uppercase: vét hoa all text

-- white-space: khoảng trắng
value:
  + normal: default
  + nowrap: không xuống dòng(kể cả chạm tới lề)
  + pre: giữ nguyên định dạng code, giống <pre>

-- word-break:beak-all; dùng để bẻ text or link xuống hàng khi nhập dài liền nhau có thể vỡ UI vì text ko bị xuống dòng 
 
-- text-shadow: đổ bóng text

-- overflow: auto // ngắn -> ko tạo thanh cuộn , dài -> tạo thanh cuộn(scrollbar)

-- text-overflow: ellipsis// tạo dấu '...'

+ background-size: - điều chỉnh kích thước ảnh nền
value:
 - cover: Ảnh khớp với khung hình, giữ nguyên tỷ lệ ảnh(ko bị méo)
 - contain: Ảnh vừa khung hình , giữ nguyên tỷ lệ ảnh
 
+ background-position: - Vị trí bắt đầu đặt ảnh nền
value:
   left,right,top,bottom,top left,top right,bottom left, bottom right, center

+ background-image: linear-gradient(direction, color-stop1, color-stop2, ...) - hiệu ứng chuyển màu

1. direction: to bottom(default) - hướng từ trên xuống

2. direction: to top - hướng từ dưới lên

3. direction: to left - hướng phải sang trái

4. direction: to right - hướng trái sang phải

...

👀giá trị % của color-stop1, color-stop2 là số % không bị chuyển màu 

+ background-attachment:
value:
 - scroll(default): ảnh tự động cuộn theo trình duyệt khi kéo lên xuống
 - fixed: Ảnh cố định khi kéo scroll lên xuống
 - local: ảnh cố định cục bộ trong bố cục con 

+ background-clip: - quy định vùng đổ nền
value:
 - Border-box(default): Ảnh sẽ đổ full kích thước phần tử (content + padding + border)
 - padding-box: Ảnh đổ từ padding tới content
 - content-box: Ảnh chỉ đổ phần content
 - text- Đổ màu nền cho text


+ background-origin: - xác định gốc bức ảnh đặt ở vị trí nào
value:
 -  Border-box: Gốc 0,0 của ảnh sẽ ở border
 - padding-box(default): Gốc ảnh mặc định ở phần padding
 - Content-box: Gốc 0,0 của ảnh ở phần content
 