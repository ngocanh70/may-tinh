<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Máy tính bỏ túi</title>
  <link rel="stylesheet" href="calculator.css" />  
</head>
<body>
   <div class="container">
    <h1>WELLCOME TO MY FIRST WEBSITE :33</h1>
    <h1>Máy Tính Đơn Giản</h1>
    <div class="calculator">
<input type="text" class="display" id="display" readonly>
      <div class="buttons">
      <button>C</button>
      <button>←</button>
      <button>%</button>
      <button>/</button>

      <button>7</button>
      <button>8</button>
      <button>9</button>
      <button>*</button>

      <button>4</button>
      <button>5</button>
      <button>6</button>
      <button>-</button>

      <button>1</button>
      <button>2</button>
      <button>3</button>
      <button>+</button>

      <button>0</button>
      <button>.</button>
      <button>=</button>
      </div>
    </div>
  </div>
</body>
<script>
  const display = document.getElementById('display');
  const buttons = document.querySelectorAll('.buttons button');

  buttons.forEach(button => {
    button.addEventListener('click', () => {
      const value = button.textContent;

      if (value === 'C') {
        display.value = ''; // Xóa màn hình
      } else if (value === '=') {
        try {
          display.value = eval(display.value); // Tính toán
        } catch {
          display.value = 'Error';
        }
      } else {
        display.value += value; // Thêm số hoặc phép tính vào chuỗi
      }
    });
  });
</script>

</html>
