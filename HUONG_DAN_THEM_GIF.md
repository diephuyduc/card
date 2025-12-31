# 🎨 HƯỚNG DẪN THÊM ẢNH (GIF, PNG, JPG, WEBP, LOTTIE)

## 🖼️ Định dạng được hỗ trợ

✅ **GIF** - Ảnh động (animated)  
✅ **PNG** - Ảnh trong suốt, chất lượng cao  
✅ **JPG/JPEG** - Ảnh nén, dung lượng nhỏ  
✅ **WEBP** - Ảnh hiện đại, tối ưu web  
✅ **Lottie JSON** - Animation vector chất lượng cao, nhẹ

## 📁 Cấu trúc thư mục

```
D:\Project\MyApplication4\birthday\
├── birthday_card.html
├── images\              ← Thư mục chứa ảnh & animation
│   ├── 1.gif           ← Ảnh GIF động
│   ├── 2.png           ← Ảnh PNG trong suốt
│   ├── 3.jpg           ← Ảnh JPG
│   ├── 4.webp          ← Ảnh WEBP
│   ├── 5.json          ← Lottie animation (JSON)
│   ├── cat.png         ← Tên tùy chỉnh
│   ├── balloon.gif
│   ├── star.json       ← Lottie star animation
│   └── ...thêm nhiều file
├── cat_show.json
└── cat_out.json
```

## 🚀 Cách sử dụng

### Bước 1: Thêm ảnh/animation vào thư mục

1. Đặt tất cả file ảnh/animation vào thư mục **`images/`**
2. Hỗ trợ các định dạng: **GIF, PNG, JPG, JPEG, WEBP, JSON (Lottie)**
3. Đặt tên file theo số hoặc tên bất kỳ:
   - Ảnh: `1.gif`, `2.png`, `3.jpg`, `4.webp`, ...
   - Lottie: `star.json`, `heart.json`, `confetti.json`, ...
   - Tùy chỉnh: `cat.png`, `party.gif`, `cake.jpg`, `balloon.json`, ...

### Bước 2: Cập nhật danh sách trong code

Mở file `birthday_card.html`, tìm dòng (~2860):

```javascript
const imageFiles = [
  { type: 'gif', src: 'images/cat_in_a_rocket.gif' },
  { type: 'gif', src: 'images/live-chatbot.gif' },
  // { type: 'png', src: 'images/balloon.png' },
  // { type: 'jpg', src: 'images/cake.jpg' },
  // { type: 'lottie', src: 'images/star.json' },
  // Thêm nhiều file tại đây...
];
```

**Thêm file ảnh/animation mới:**
```javascript
const imageFiles = [
  // GIF động
  { type: 'gif', src: 'images/cat_in_a_rocket.gif' },
  { type: 'gif', src: 'images/live-chatbot.gif' },
  { type: 'gif', src: 'images/party.gif' },
  
  // PNG trong suốt
  { type: 'png', src: 'images/balloon.png' },
  { type: 'png', src: 'images/star.png' },
  
  // JPG
  { type: 'jpg', src: 'images/cake.jpg' },
  
  // WEBP
  { type: 'webp', src: 'images/confetti.webp' },
  
  // Lottie JSON (animation vector)
  { type: 'lottie', src: 'images/star.json' },
  { type: 'lottie', src: 'images/heart.json' },
  { type: 'lottie', src: 'images/firework.json' }
];
```

**Lưu ý định dạng:**
- `type: 'gif'` - cho file .gif
- `type: 'png'` - cho file .png
- `type: 'jpg'` - cho file .jpg hoặc .jpeg
- `type: 'webp'` - cho file .webp
- `type: 'lottie'` - cho file .json (Lottie animation)

### Bước 3: Lưu và test

1. Lưu file HTML
2. Refresh trình duyệt (Ctrl + F5)
3. Xem ảnh bay ngẫu nhiên! 🎉

## 🎨 Tùy chỉnh hiệu ứng

### 1. Thay đổi tốc độ xuất hiện

Tìm dòng:
```javascript
const imageInterval = setInterval(createRandomImage, 800);
```

Thay đổi `800` (miligiây):
- `500` = Nhanh hơn (0.5 giây/1 ảnh)
- `1000` = Chậm hơn (1 giây/1 ảnh)
- `1500` = Rất chậm (1.5 giây/1 ảnh)

### 2. Thay đổi số lượng ảnh ban đầu

Tìm dòng:
```javascript
for (let i = 0; i < 15; i++) {
  setTimeout(createRandomImage, i * 100);
}
```

Thay đổi `15` thành số lượng bạn muốn:
- `10` = Ít ảnh hơn
- `20` = Nhiều ảnh hơn
- `30` = Rất nhiều ảnh

### 3. Thay đổi kích thước ảnh

Tìm dòng:
```javascript
width: ${80 + Math.random() * 120}px;
```

Thay đổi công thức:
- `${50 + Math.random() * 80}px` = Ảnh nhỏ hơn (50-130px)
- `${100 + Math.random() * 150}px` = Ảnh lớn hơn (100-250px)
- `${150 + Math.random() * 200}px` = Ảnh rất lớn (150-350px)

### 4. Thay đổi tốc độ rơi

Tìm dòng:
```javascript
const duration = 8000 + Math.random() * 4000;
```

Thay đổi giá trị (miligiây):
- `5000 + Math.random() * 2000` = Rơi nhanh (5-7 giây)
- `10000 + Math.random() * 5000` = Rơi chậm (10-15 giây)

### 5. Thay đổi độ trong suốt

Tìm dòng:
```javascript
opacity: ${0.7 + Math.random() * 0.3};
```

Thay đổi công thức:
- `${0.5 + Math.random() * 0.3}` = Mờ hơn (0.5-0.8)
- `${0.9 + Math.random() * 0.1}` = Rõ hơn (0.9-1.0)
- `1` = Hoàn toàn rõ nét

## 💡 Mẹo hay

### Sử dụng ảnh chất lượng cao:

1. **Kích thước phù hợp**: 200-500px (không quá lớn)
2. **Dung lượng**: 
   - GIF: Dưới 2MB
   - PNG: Dưới 1MB (dùng cho ảnh trong suốt)
   - JPG: Dưới 500KB (dùng cho ảnh nền)
   - WEBP: Dưới 500KB (tối ưu nhất)
3. **Định dạng phù hợp**:
   - GIF: Ảnh động, hoạt hình
   - PNG: Ảnh trong suốt (transparent), logo, icon
   - JPG: Ảnh có nền, ảnh chất lượng cao
   - WEBP: Hiện đại, nhẹ, nhanh
4. **Nội dung**: Trong suốt (PNG), hoạt hình (GIF), vui nhộn

### Nguồn tải ảnh miễn phí:

**GIF động:**
- 🔥 **GIPHY**: https://giphy.com/
- 🎨 **Tenor**: https://tenor.com/
- 🌟 **Flaticon**: https://www.flaticon.com/animated-icons
- 🎭 **LottieFiles**: https://lottiefiles.com/ (chuyển sang GIF)

**PNG trong suốt:**
- 🖼️ **PNGTree**: https://pngtree.com/
- 🎨 **Freepik**: https://www.freepik.com/
- 🌟 **Flaticon**: https://www.flaticon.com/
- 🎭 **Vecteezy**: https://www.vecteezy.com/

**Ảnh JPG/WEBP:**
- 📸 **Unsplash**: https://unsplash.com/
- 🖼️ **Pexels**: https://www.pexels.com/
- 🌟 **Pixabay**: https://pixabay.com/

**Lottie Animation (JSON):**
- 🎨 **LottieFiles**: https://lottiefiles.com/
- 🌟 **IconScout**: https://iconscout.com/lottie-animations
- 🎭 **Lordicon**: https://lordicon.com/

### Ưu điểm của Lottie:

✅ **Nhẹ hơn GIF** - File JSON nhỏ hơn nhiều lần  
✅ **Chất lượng cao** - Vector, không bị vỡ khi phóng to  
✅ **Tương tác tốt** - Có thể điều khiển animation  
✅ **Load nhanh** - Tối ưu cho web  
✅ **Màu sắc đẹp** - Không bị giảm chất lượng

### Chủ đề ảnh/animation gợi ý:

- 🎂 Bánh sinh nhật (GIF hoặc PNG)
- 🎈 Bóng bay (PNG trong suốt)
- 🎉 Pháo hoa (GIF động)
- 🎁 Quà tặng (PNG trong suốt)
- 🐱 Mèo dễ thương (GIF hoặc PNG)
- 🦄 Kỳ lân (PNG trong suốt)
- ⭐ Ngôi sao lấp lánh (GIF động)
- 🌈 Cầu vồng (PNG trong suốt)
- 🎊 Confetti (GIF động)
- 💖 Trái tim (PNG hoặc GIF)

## 🔧 Tính năng nâng cao

### Nhóm ảnh theo chủ đề:

```javascript
const birthdayImages = [
  'images/cake1.gif',        // GIF động
  'images/cake2.png',        // PNG trong suốt
  'images/balloon1.gif'      // GIF động
];

const cuteImages = [
  'images/cat1.png',         // PNG trong suốt
  'images/unicorn1.gif'      // GIF động
];

const partyImages = [
  'images/firework1.gif',    // GIF động
  'images/confetti1.png',    // PNG trong suốt
  'images/star.webp'         // WEBP hiện đại
];

// Random từ tất cả nhóm
const allImages = [...birthdayImages, ...cuteImages, ...partyImages];
```

### Chỉ hiển thị ảnh ở màn cụ thể:

```javascript
// Chỉ hiển thị khi vào màn lời chúc
function transitionToWishesScreen() {
  // ...existing code...
  
  // Tăng cường hiệu ứng ảnh
  for (let i = 0; i < 20; i++) {
    setTimeout(createRandomImage, i * 100);
  }
}
```

## ❌ Xử lý lỗi

### Lỗi: Ảnh không hiển thị

**Nguyên nhân:**
- Đường dẫn file sai
- File không tồn tại trong thư mục `images/`

**Giải pháp:**
1. Kiểm tra tên file trong code khớp với file thực tế
2. Đảm bảo file ở đúng thư mục `images/`
3. Mở Console (F12) xem lỗi chi tiết

### Lỗi: Ảnh load chậm

**Nguyên nhân:**
- File ảnh quá lớn

**Giải pháp:**
1. Nén file:
   - GIF: https://ezgif.com/optimize
   - PNG: https://tinypng.com/
   - JPG: https://compressjpeg.com/
2. Giảm kích thước ảnh xuống dưới 500KB
3. Giảm số lượng ảnh xuất hiện cùng lúc

### Lỗi: Trang bị lag

**Nguyên nhân:**
- Quá nhiều ảnh chạy cùng lúc

**Giải pháp:**
1. Giảm tốc độ: `setInterval(createRandomImage, 1500)`
2. Giảm số lượng ban đầu: `for (let i = 0; i < 8; i++)`
3. Tăng thời gian animation để ảnh tồn tại ít hơn

## 🎯 Kết quả

Sau khi hoàn tất, bạn sẽ có:
- ✅ Ảnh (GIF, PNG, JPG, WEBP) bay ngẫu nhiên khắp màn hình
- ✅ Hiệu ứng mượt mà, đẹp mắt
- ✅ Tùy chỉnh linh hoạt
- ✅ Dễ dàng thêm/bớt ảnh
- ✅ Hỗ trợ đa định dạng ảnh

**Chúc bạn thành công! 🎉**

