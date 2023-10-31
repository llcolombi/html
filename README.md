<!DOCTYPE html>
<html>
<head>
  <title>Calculadora de Lucas Colombi</title>
  <style>
    body {
      font-family: Times New Roman, Times New Roman;
    }
    .calculator {
      width: 300px;
      margin: 0 auto;
      background-color: #f2f2f2;
      border: 1px solid #ccc;
      border-radius: 5px;
      padding: 10px;
    }
    .output {
      text-align: right;
      font-size: 24px;
      margin-bottom: 10px;
    }
    .btn {
      width: 70px;
      height: 50px;
      font-size: 20px;
      margin: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
    <h2>Lucas Colombi</h2>
        <h3>Estudante de sistemas de informação - Estácio de Sá</h3>
        <body>
  <div class="calculator">
    <div class="output" id="output">0</div>
    <button class="btn" onclick="clearOutput()">C</button>
    <button class="btn" onclick="appendToOutput('2')">2</button>
    <button class="btn" onclick="appendToOutput('3')">3</button>
    <button class="btn" onclick="appendToOutput('4')">4</button>
    <button class="btn" onclick="appendToOutput('5')">5</button>
    <button class="btn" onclick="appendToOutput('6')">6</button>
    <button class="btn" onclick="appendToOutput('7')">7</button>
    <button class="btn" onclick="appendToOutput('8')">8</button>
    <button class="btn" onclick="appendToOutput('9')">9</button>
    <button class="btn" onclick="appendToOutput('-')">-</button>
    <button class="btn" onclick="appendToOutput('+')">+</button>
    <button class="btn" onclick="appendToOutput('1')">1</button>
    <button class="btn" onclick="appendToOutput('')"></button>
    <button class="btn" onclick="appendToOutput('0')">0</button>
    <button class="btn" onclick="calculateResult()">=</button>
    <button class="btn" onclick="appendToOutput('/')">/</button>
  </div>

  <script>
    function clearOutput() {
      document.getElementById("output").innerText = "0";
    }

    function appendToOutput(value) {
      const output = document.getElementById("output");
      if (output.innerText === "0" && value !== "C") {
        output.innerText = value;
      } else {
        output.innerText += value;
      }
    }

    function calculateResult() {
      const output = document.getElementById("output");
      try {
        output.innerText = eval(output.innerText);
      } catch (error) {
        output.innerText = "Erro";
      }
    }
  </script>
</body>
</html>

<!DOCTYPE html
<html>
<head>
  <title>Formulário de Lucas Colombi </title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    .form-container {
      margin: 0 auto;
      padding: 20px;
      background-color: #f2f2f2;
      border: 1px solid #ccc;
      border-radius: 10px;
    }
    .form-group {
      margin-bottom: 20px;
    }
    .form-group label {
      font-weight: bold;
      display: block;
    }
    .form-group input[type="text"] {
      width: calc(100% - 20px);
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 5px;
      transition: width 0.3s;
    }
    .form-group input[type="text"]:focus {
      width: calc(100% - 40px);
    }
    .form-group textarea {
      width: calc(100% - 20px);
      padding: 10px;
      font-size: 16px;
      border: 1px solid #ccc;
      border-radius: 5px;
      transition: width 0.3s;
    }
    .form-group textarea:focus {
      width: calc(100% - 40px);
    }
    .form-group button {
      background-color: #4caf50;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .form-group button:hover {
      background-color: #45a049;
    }
  </style>
</head>
<h2>Formulário de Lucas Colombi</h2>
        <h3>Estudante de sistemas de informação - Estácio de Sá</h3>
<body>
  <div class="form-container">
    <div class="form-group">
      <label for="name">Nome:</label>
      <input type="text" id="name" placeholder="Digite seu nome">
    </div>
    <div class="form-group">
      <label for="email">Email:</label>
      <input type="text" id="email" placeholder="Digite seu email">
    </div>
    <div class="form-group">
      <label for="message">Mensagem:</label>
      <textarea id="message" placeholder="Digite sua mensagem"></textarea>
    </div>
    <div class="form-group">
      <button onclick="submitForm()">Enviar</button>
    </div>
  </div>

  <script>
    function submitForm() {
      var name = document.getElementById("name").value;
      var email = document.getElementById("email").value;
      var message = document.getElementById("message").value;

      if (name === "" || email === "" || message === "") {
        alert("Por favor, preencha todos os campos.");
      } else {
        // Aqui você pode enviar os dados do formulário para o servidor ou realizar outras ações com os dados.
        alert("Formulário enviado com sucesso!");
        // Resetar o formulário após o envio, se desejado
        document.getElementById("name").value = "";
        document.getElementById("email").value = "";
        document.getElementById("message").value = "";
      }
    }
  </script>
</body>
</html>
