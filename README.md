# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419 <br>
## BÀI TẬP LỚN:<br>
I. Viết phần mềm trên công cụ Mit App inventor:<br>
   - Tạo dự án:<br>
  <img width="335" height="274" alt="image" src="https://github.com/user-attachments/assets/55a18f3b-596b-492a-ae82-70866812bc68" />
<br>
- Thêm 2 Screen:<br>
  <img width="941" height="814" alt="image" src="https://github.com/user-attachments/assets/b9fa343d-cd86-4751-83f9-47bd0f731b7e" />
<br>
- Cấu hình Screen1 about về bản thân+nút gọi sang 2 screen còn lại<br>
  + Sử dụng các thanh công cụ trong User Interface để cấu hình giao diện:<br>
  + Kéo thanh label vào màn hình và sử đổi phần text trong cột Properties thành nôi dung muốn hiển thị, Kéo 2 button để thực hiện chuyển hướng sang các screen còn lại<br>
<img width="1419" height="836" alt="image" src="https://github.com/user-attachments/assets/b15c46e4-b894-4e94-9128-0e3a769fbebb" />
<br>

- Cấu hình Screen2 bằng giao diện đồ họa( giải bài toán đơn giản)<br>
  + Tiếp tục sử dụng các thanh label để hiển thị, button để thực hiện tính toán, textbox để nhập giá trị<br>
  <img width="1340" height="801" alt="image" src="https://github.com/user-attachments/assets/3fe55091-dc03-46d2-8c61-e08880ca5863" />
<br>

- Cấu hình Screen3 bằng giao diện đồ họa( truy cập webview có sẵn)<br>
  + Thêm công cụ web view vào screen3<br>
  + Dán url trang web vào HomeUrl<br>
<img width="1899" height="897" alt="image" src="https://github.com/user-attachments/assets/0f51aff0-eeb6-4e9d-849f-84a37cd84d27" />


- Cấu hình Screen1 bằng block để xử lí logic:<br>
  + Chọn 2 khối điều kiện When button click do open another screen:<br>
    <img width="873" height="127" alt="image" src="https://github.com/user-attachments/assets/820dab33-e0fe-4928-965f-21581db8e35e" />
<br>
- Cấu hình Screen2 bằng block:<br>
<img width="979" height="402" alt="image" src="https://github.com/user-attachments/assets/d1a460f3-f3c2-401f-862e-1f8e0545071e" />
<br>

  - Screen3 không cần cấu hình gì thêm vì đã thêm url rồi<br>
 
  - Kết nối tới Mitt App APK trêm điện thoại để test:<br>
    
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/a8aaa4d2-25eb-4cc7-99ba-de79d611ef43" />
<br>
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/d6e90663-7756-4487-9835-af6d8b763625" />
<br>
<img width="1290" height="2796" alt="image" src="https://github.com/user-attachments/assets/c3e28806-7d2f-4413-ae85-01a35b21b3ea" />
<br>
  - Bản chất của việc kéo thả Block<br>
Trong MIT App Inventor, lập trình được thực hiện bằng cách kéo và ghép các khối lệnh (Blocks) thay vì viết mã nguồn bằng ngôn ngữ lập trình. Mỗi block đại diện cho một câu lệnh, điều kiện, phép toán hoặc sự kiện. Khi ghép các block lại với nhau, ta tạo thành logic hoạt động của chương trình.<br>

a. Ưu điểm so với viết code<br>
- Dễ học và dễ sử dụng cho người mới bắt đầu.<br>
- Hạn chế lỗi cú pháp vì các block chỉ ghép được theo cấu trúc hợp lệ.<br>
- Trực quan, dễ quan sát luồng xử lý của chương trình.<br>
- Tăng tốc độ phát triển các ứng dụng đơn giản.<br>
- Phù hợp cho việc học tư duy lập trình và phát triển ứng dụng nhanh.<br>
b. Nhược điểm<br>
- Khó xây dựng các ứng dụng lớn và phức tạp.<br>
- Khi chương trình nhiều chức năng, số lượng block lớn sẽ gây rối và khó quản lý.<br>
- Ít linh hoạt hơn so với các ngôn ngữ lập trình truyền thống như Java, Python, Kotlin.<br>
- Khả năng tối ưu và mở rộng bị hạn chế.<br>
- Khó tích hợp các thư viện hoặc chức năng nâng cao.<br>
                  
II. Viết app sử dụng Android Studio<br>
   # 1. AndroidManifest.xml là gì?<br>

`AndroidManifest.xml` là file cấu hình trung tâm của ứng dụng Android.<br>

Nó dùng để mô tả:<br>

- Tên package của ứng dụng.<br>
- Các Activity, Service, Broadcast Receiver.<br>
- Các quyền (Permission) ứng dụng cần sử dụng.<br>
- Phiên bản Android hỗ trợ.<br>
- Icon, Theme, Launcher Activity,...<br>

## Khai báo quyền<br>

Ví dụ quyền Internet:<br>

```xml
<uses-permission android:name="android.permission.INTERNET"/>
```

Ví dụ quyền vị trí:<br>

```xml
<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
```

## Mục đích<br>

Android sử dụng Manifest để:<br>

- Xác định cấu trúc ứng dụng.<br>
- Kiểm soát bảo mật.<br>
- Cấp phát quyền truy cập tài nguyên hệ thống.<br>


# 2. Vòng đời của Activity Android<br>

```text
onCreate()
↓
onStart()
↓
onResume()
↓
(Ứng dụng hoạt động)

↓
onPause()
↓
onStop()

↓
onRestart()
↓
onStart()
↓
onResume()

hoặc

onDestroy()
```

## Ý nghĩa các hàm<br>

### onCreate()<br>

Được gọi khi Activity được tạo lần đầu.<br>

Thường dùng để:<br>

- Nạp giao diện.<br>
- Khởi tạo biến.<br>
- Khởi tạo dữ liệu.<br>

### onStart()<br>

Activity bắt đầu hiển thị.<br>

### onResume()<br>

Activity ở trạng thái tương tác với người dùng.<br>

### onPause()<br>

Activity bị che một phần hoặc mất focus.<br>

### onStop()<br>

Activity không còn hiển thị.<br>

### onDestroy()<br>

Activity bị hủy hoàn toàn.<br>

# 3. Tại sao Android Studio sinh sẵn hàm onCreate()?<br>

Android Framework tự động gọi `onCreate()` khi Activity được tạo.<br>

Do hầu hết ứng dụng đều cần:<br>

- Nạp giao diện.<br>
- Khởi tạo dữ liệu.<br>

nên Android Studio tạo sẵn:<br>

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
}
```
# 4. Kiểm tra quyền trong Android<br>

Từ Android 6.0 trở lên phải kiểm tra Runtime Permission.<br>

Ví dụ kiểm tra quyền Camera:<br>

```java
if (ContextCompat.checkSelfPermission(
        this,
        Manifest.permission.CAMERA)
        != PackageManager.PERMISSION_GRANTED) {

    ActivityCompat.requestPermissions(
            this,
            new String[]{Manifest.permission.CAMERA},
            100);
}
```

## Ý nghĩa<br>

### checkSelfPermission()<br>

Kiểm tra ứng dụng đã được cấp quyền hay chưa.<br>

### requestPermissions()<br>

Hiển thị hộp thoại yêu cầu người dùng cấp quyền.<br>


# 5. Giao diện Android<br>

Giao diện được mô tả bằng file XML nằm trong:<br>

```text
res/layout
```

Ví dụ:<br>

```xml
<TextView
    android:id="@+id/txtName"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

# 6. Tránh Hardcode Text<br>

Không nên:<br>

```xml
android:text="Xin chào"
```

Nên lưu trong:<br>

```text
res/values/strings.xml
```

Ví dụ:<br>

```xml
<string name="hello">Xin chào</string>
```

Sử dụng:<br>

```xml
android:text="@string/hello"
```

# 7. Cú pháp tham chiếu tài nguyên<br>

## String<br>

```xml
@string/hello
```

## Color<br>

```xml
@color/primary
```

## Drawable<br>

```xml
@drawable/logo
```

## Dimension<br>

```xml
@dimen/text_size
```

# 8. Ưu điểm của việc tham chiếu tài nguyên<br>

- Dễ bảo trì.<br>
- Tránh lặp dữ liệu.<br>
- Hỗ trợ đa ngôn ngữ.<br>
- Hỗ trợ nhiều giao diện.<br>
- Dễ thay đổi nội dung tập trung.<br>

# 9. Android tự động chọn tài nguyên theo Language, Location, Theme<br>

Ví dụ:<br>

```text
values/
values-vi/
values-en/
```

Android sẽ tự động chọn:<br>

- values-vi → khi máy dùng tiếng Việt.<br>
- values-en → khi máy dùng tiếng Anh.<br>

Ví dụ Dark Mode:<br>

```text
values/
values-night/
```

Android sẽ tự động chọn giao diện phù hợp.<br>


# 10. Lợi ích của việc tự động chọn tài nguyên<br>

Ứng dụng có thể:<br>

- Tự đổi ngôn ngữ.<br>
- Tự đổi giao diện sáng/tối.<br>
- Tự thay đổi tài nguyên theo cấu hình thiết bị.<br>
- Hỗ trợ quốc tế hóa (Internationalization).<br>

# 11. Đối tượng chứa (Layout Container)<br>

Layout là đối tượng dùng để chứa và sắp xếp các View con.<br>

Ví dụ:<br>

- LinearLayout<br>
- RelativeLayout<br>
- ConstraintLayout<br>
- FrameLayout<br>

# 12. LinearLayout<br>

## Sắp xếp theo chiều dọc<br>

```xml
android:orientation="vertical"
```

Ví dụ:<br>

```text
Button
TextView
EditText
```

## Sắp xếp theo chiều ngang<br>

```xml
android:orientation="horizontal"
```

Ví dụ:<br>

```text
Button Button Button
```

# 13. Gravity<br>

Gravity quy định vị trí hiển thị của các View bên trong Layout.<br>

Ví dụ:<br>

```xml
android:gravity="center"
```

Các giá trị phổ biến:<br>

```text
center
left
right
top
bottom
center_horizontal
center_vertical
```

# 14. Code tương tác với Layout<br>

Ví dụ lấy TextView:<br>

```java
TextView txt = findViewById(R.id.txtName);
```

Hiển thị nội dung:<br>

```java
txt.setText(R.string.hello);
```

# 15. Tại sao dùng R.string thay vì Hardcode?<br>

Không nên:<br>

```java
txt.setText("Xin chào");
```

Nên:<br>

```java
txt.setText(R.string.hello);
```

Vì Android sẽ tự động lấy:<br>

- Ngôn ngữ phù hợp.<br>
- Theme phù hợp.<br>
- Tài nguyên phù hợp với thiết bị.<br>


# 16. Event là gì?<br>

Event là các sự kiện do người dùng tác động vào ứng dụng.<br>

Ví dụ:<br>

- Click Button.<br>
- Click TextView.<br>
- Chạm màn hình.<br>
- Nhập dữ liệu.<br>
- Vuốt màn hình.<br>


# 17. Layout cần làm gì để xử lý Event?<br>

Cần khai báo ID cho View:<br>

```xml
<Button
    android:id="@+id/btnSubmit"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

Sau đó code Java có thể truy cập View bằng:<br>

```java
findViewById(R.id.btnSubmit);
```

# 18. Xử lý Event - Cách 1: Listener trong Java<br>

```java
Button btn = findViewById(R.id.btnSubmit);

btn.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        // xử lý sự kiện
    }
});
```

## Ưu điểm<br>

- Phổ biến nhất.<br>
- Dễ quản lý.<br>
- Phù hợp dự án lớn.<br>

# 19. Xử lý Event - Cách 2: Khai báo trực tiếp trong XML<br>

## XML<br>

```xml
<Button
    android:onClick="submitData"/>
```

## Java<br>

```java
public void submitData(View view) {
    // xử lý sự kiện
}
```

## Ưu điểm<br>

- Viết nhanh.<br>
- Phù hợp ứng dụng nhỏ.<br>

## Nhược điểm<br>

- Khó quản lý khi dự án lớn.<br>
- Không linh hoạt bằng Listener.<br>
     trong app có các thư mục đặc biệt: Assets<br>
     khi sử dụng Window Explorer để copy các files + folder vào trong Assets<br>
     thì khi compiler: mọi file này đều đi theo app, nằm trong app<br>
     trong app có thể truy cập được đến các file này<br>
     cú pháp truy cập vào là gì?<br>
     lợi ích của việc app có sẵn các files (offline cũng có)?<br>
     ứng dụng: app hướng dẫn việc X<br>


III. Cài đặt app:<br>
1. App1:<br>
ĐẶT VẤN ĐỀ & PHƯƠNG PHÁP GIẢI QUYẾTVấn đề: Ban cán sự lớp cần một ứng dụng offline quản lý danh sách sinh viên lớp 58KTP để điểm danh hoặc tra cứu nhanh số điện thoại khi mất mạng.
Tuy nhiên, dữ liệu thô ban đầu được lưu lộn xộn, không theo thứ tự bảng chữ cái (Alphabet) của Tên sinh viên, gây khó khăn cho việc tra cứu thủ công.
Giải pháp xử lý & Thuật toán:Lưu trữ: Chuẩn bị trước file students.json lưu trong thư mục assets.
Thuật toán tiền xử lý: Sử dụng Thuật toán sắp xếp nổi bọt (Bubble Sort) hoặc Collections.sort() dựa trên một Comparator tùy biến để tự động bóc tách Chữ cái đầu tiên của Tên (Không tính Họ và Tên đệm) để sắp xếp lại danh sách theo thứ tự từ A --> Z ngay khi nạp ứng dụng.
Đối tượng hiển thị: Sử dụng ListView kết hợp với SimpleAdapter để hiển thị dữ liệu dạng hai dòng (Tên sinh viên làm tiêu đề chính, Mã sinh viên & SĐT làm tiêu đề phụ) một cách tối giản, trực quan.

Triển Khai các bước trên android studio:
Bước 1: Khởi tạo cấu trúc thư mục và file dữ liệu Assets
<img width="989" height="664" alt="image" src="https://github.com/user-attachments/assets/cf649434-bff4-415f-878d-6317aabf0482" />
Bước 2: Thiết kế giao diện chính (activity_main.xml)
<img width="934" height="703" alt="image" src="https://github.com/user-attachments/assets/528ea89c-faa1-45f0-bd99-7d4da05201bd" />
Bước 3: Tạo khuôn mẫu đối tượng dữ liệu (Student.java)

<img width="1161" height="740" alt="image" src="https://github.com/user-attachments/assets/1fe63894-39f6-438e-9462-10723392a61f" />
Bước 4: Viết logic đọc, xử lý thuật toán tại MainActivity.java

<img width="854" height="899" alt="image" src="https://github.com/user-attachments/assets/7834aa6a-3bde-4b96-bf15-3404d58e58f6" />

Bước 5: Cài đặt và kiểm thử( tắt internet):

<img width="552" height="978" alt="image" src="https://github.com/user-attachments/assets/ec0e115a-6d95-4eba-a880-a6b99f9fd4a2" />

1. ĐẶC THÙ CỦA DỮ LIỆU (Mô tả dữ liệu)
Định dạng lưu trữ: Dữ liệu thuộc loại dữ liệu có cấu trúc (Structured Data), được chuẩn hóa theo định dạng cặp Key - Value của tệp tin students.json lưu cục bộ trong thư mục assets.

Bảng mã hiển thị: Sử dụng cấu trúc mã hóa ký tự UTF-8, đảm bảo toàn bộ họ tên tiếng Việt có dấu của 71 sinh viên không bị lỗi font khi hệ thống bóc tách luồng dữ liệu thô.

Tính chất hỗn hợp: Dữ liệu chứa cả các trường định danh cố định (Mã sinh viên - msv, Họ tên - name, Số điện thoại - phone) kết hợp với dữ liệu số nguyên biến động tích hợp sẵn là số lần tương tác (visits).

Sự lộn xộn ban đầu: Thứ tự các dòng sinh viên trong tệp tĩnh được sắp xếp ngẫu nhiên theo mã sinh viên, hoàn toàn không tuân theo quy tắc sắp xếp danh sách lớp truyền thống của Việt Nam.
2. THUẬT TOÁN TIỀN XỬ LÝ DỮ LIỆU
Ứng dụng triển khai kết hợp hai giải pháp thuật toán để tối ưu hóa dữ liệu trước khi render lên màn hình giao diện:
Thuật toán Tách chuỗi (String Tokenization / Substring):
Nguyên lý: Sử dụng hàm toán thuật tự chế getFirstNameOnly() dựa vào vị trí khoảng trắng cuối cùng (lastIndexOf(" ")) để cắt bỏ hoàn toàn phần Họ và Tên đệm.
Mục đích: Trích xuất ra duy nhất Tên chính của sinh viên (Ví dụ: "Lê Tuấn Anh" ---> "Anh").
Thuật toán Sắp xếp (Sorting Algorithm):
Nguyên lý: Sử dụng phương thức Collections.sort() áp dụng cấu trúc TimSort (kết hợp giữa Merge Sort và Insertion Sort) với một bộ so sánh Comparator tùy biến không phân biệt chữ hoa chữ thường (compareToIgnoreCase).
Mục đích: Ép danh sách mảng (ArrayList) tự động đảo vị trí các đối tượng sinh viên dựa trên Tên chính đã tách, đưa toàn bộ danh sách lớp về chuẩn Alphabet từ A --> Z một cách logic (Sinh viên tên "Anh" luôn đứng đầu, sinh viên tên "Việt" tự động xuống cuối).


3. App2:<br>
- Bước 1: Khởi tạo dự án mới:<br>
  <img width="982" height="797" alt="image" src="https://github.com/user-attachments/assets/749dd4e7-beb2-4e19-bc8a-39cafe0e4848" /><br>

- Bước 2: Cấp quyền Internet (AndroidManifest.xml)<br>
   <img width="895" height="687" alt="image" src="https://github.com/user-attachments/assets/93e7d885-d1a5-4d2a-883f-f59f93f6362a" /><br>

- Bước 3: Thiết kế Giao diện (XML):<br>
  1. Activity 1: Giới thiệu bản thân (activity_main.xml)<br>
     Giao diện gồm thông tin cá nhân và 2 nút để chuyển sang Activity 2 và Activity 3.<br>
  <img width="841" height="686" alt="image" src="https://github.com/user-attachments/assets/312018ef-8b47-43e8-a553-7602ff4a7591" />
<br>

   2. Activity 2: Giải toán + Gọi API (activity_math.xml)<br>
      Click chuột phải vào thư mục layout --> New --> Layout Resource File--> Đặt tên là activity_math.<br>
<img width="412" height="284" alt="image" src="https://github.com/user-attachments/assets/6c18aef4-5f7f-46f2-a36b-affb35b24190" /><br>
<img width="825" height="769" alt="image" src="https://github.com/user-attachments/assets/b0963d98-9ea1-4b24-a459-18d4e9fd9373" />
<br>
   3. Activity 3: WebView hiển thị trang web (activity_web.xml):<br>
   <img width="836" height="328" alt="image" src="https://github.com/user-attachments/assets/6d62010c-7c0b-4365-8864-af8c0bcedda6" />
<br>

- Bước 4: Viết Logic xử lý (Java):<br>
  1. MainActivity.java (Điều hướng):<br>
     <img width="860" height="594" alt="image" src="https://github.com/user-attachments/assets/7c97cfd6-b411-4d73-bf76-41c2ce32321a" /><br>
2. MathActivity.java:<br>
  <img width="827" height="738" alt="image" src="https://github.com/user-attachments/assets/6065ff3a-52bb-4fb0-9f82-e6546a0f5bc6" />
<br>
3. WebActivity.java (WebView truy cập URL định danh mã sinh viên)<br>
  <img width="840" height="765" alt="image" src="https://github.com/user-attachments/assets/fda928e8-e69c-4f5f-8b87-57e6320de2bb" />
<br>

- Bước 5: Khai báo Activity mới trong AndroidManifest.xml<br>
<img width="854" height="801" alt="image" src="https://github.com/user-attachments/assets/df3105d3-80b0-4203-a7ca-40ea9f9f764c" /><br>

- Bước 6: Tiến hành build và kiểm thử<br>
  
+ Acivity1:<br>
  <img width="558" height="636" alt="image" src="https://github.com/user-attachments/assets/f0c7bf98-c9a1-4a70-b127-69834a103bc2" />
<br>

+ Activity2:<br>
  
<img width="557" height="816" alt="image" src="https://github.com/user-attachments/assets/9c69c2b6-e28e-48f1-bf3b-e096616ec992" />
<br>

+ Activity3:<br>
<img width="562" height="446" alt="image" src="https://github.com/user-attachments/assets/d2560531-c887-43a2-bd45-90bc9d335499" />
<br>

