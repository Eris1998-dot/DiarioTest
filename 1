<!DOCTYPE html>
<!-- 
Diário de Catequese - Paróquia Nossa Senhora dos Remédios
Versão: 1.1
Data: 24/05/2024
Autor: [Seu Nome]
-->
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Diário de Catequese - Paróquia N. Sra. dos Remédios</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f2f2f2;
    }
    .container {
      background-color: white;
      padding: 30px;
      border-radius: 10px;
      max-width: 900px;
      margin: 40px auto;
      box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
    }
    h1 {
      text-align: center;
      font-size: 24px;
      margin-bottom: 20px;
    }
    label {
      display: block;
      margin-top: 15px;
      font-weight: bold;
    }
    input,
    select,
    textarea {
      width: 100%;
      padding: 10px;
      margin-top: 5px;
      border: 1px solid #ccc;
      border-radius: 5px;
      font-size: 14px;
    }
    button {
      margin-top: 20px;
      padding: 12px 20px;
      background-color: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      font-size: 14px;
    }
    button + button {
      margin-left: 10px;
    }
    table {
      width: 100%;
      margin-top: 20px;
      border-collapse: collapse;
    }
    th,
    td {
      border: 1px solid #ddd;
      padding: 10px;
      text-align: left;
      font-size: 14px;
    }
    th {
      background-color: #e6e6e6;
    }
    .presenca {
      width: 20px;
      height: 20px;
      cursor: pointer;
    }
    .presente {
      background-color: lightgreen;
    }
    .faltou {
      background-color: lightcoral;
    }
  </style>
  <!-- Bibliotecas locais em vez de CDN -->
  <script src="lib/jspdf.umd.min.js"></script>
  <script src="lib/jspdf.plugin.autotable.min.js"></script>
</head>
<body>
  <div class="container">
    <h1>Diário de Catequese<br>Paróquia Nossa Senhora dos Remédios - Diocese de Petrolina</h1>

    <label for="tipo">Tipo de Catequese:</label>
    <select id="tipo" onchange="verificarAlunos()">
      <option>Pré-Catequese</option>
      <option>Eucaristia I</option>
      <option>Eucaristia II</option>
      <option>Perseverança</option>
      <option>Crisma Jovem</option>
      <option>Crisma Adulta</option>
      <option>Adulto I</option>
      <option>Adulto II</option>
    </select>

    <label for="responsavel">Responsável:</label>
    <input type="text" id="responsavel" oninput="verificarAlunos()" />

    <label for="auxiliares">Auxiliar(es):</label>
    <input type="text" id="auxiliares" />

    <label for="leitura">Leitura do Dia (Ex: Js 6, 1-20):</label>
    <input type="text" id="leitura" />

    <label for="tema">Tema da Aula:</label>
    <input type="text" id="tema" />

    <label for="data">Data:</label>
    <input type="date" id="data" />

    <h3>Frequência</h3>
    <table id="frequencia">
      <thead>
        <tr>
          <th>Nº</th>
          <th>Nome</th>
          <th>Presença</th>
          <th>Justificativa</th>
          <th>Observações</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>

    <label for="conteudo">Conteúdo Trabalhado:</label>
    <textarea id="conteudo" rows="5"></textarea>

    <button onclick="gerarPDF()">Gerar PDF</button>
    <button onclick="limparSelecao()">Limpar Seleção</button>
  </div>

  <script>
    // Dados das turmas - pode ser movido para um arquivo separado (dados.js) no futuro
    const alunosPorCatequese = {
      "Crisma Jovem": [
        "Adila Lavinia da Costa Ferreira",
        "Adrielly Alves Costa",
        // ... (demais alunos da Crisma Jovem)
      ],
      "Eucaristia I": [
        "Alahna Monielen B. de Souza",
        "Ariany Ferreira Costa",
        // ... (demais alunos da Eucaristia I)
      ],
      "Eucaristia II": [
        "Breno Rafael Pereira Carvalho",
        "Elenice de Souza Santos",
        // ... (demais alunos da Eucaristia II)
      ]
    };

    function verificarAlunos() {
      const responsavel = document.getElementById("responsavel").value.trim();
      const tipo = document.getElementById("tipo").value;

      const frequenciaBody = document.querySelector("#frequencia tbody");
      frequenciaBody.innerHTML = "";

      // Verifica combinações de responsável e turma
      if (responsavel === "Erisvaldo de Souza Alencar" && tipo === "Crisma Jovem") {
        popularTabela("Crisma Jovem");
      } else if ((responsavel === "Maria Elena" || responsavel === "Maria Elena Viana Barbosa") && tipo === "Eucaristia I") {
        popularTabela("Eucaristia I");
      } else if (responsavel === "Mayane da Silva Lima" && tipo === "Eucaristia II") {
        popularTabela("Eucaristia II");
      }
    }

    function popularTabela(turma) {
      const frequenciaBody = document.querySelector("#frequencia tbody");
      alunosPorCatequese[turma].forEach((aluno, index) => {
        const row = document.createElement("tr");
        row.innerHTML = `
          <td>${index + 1}</td>
          <td>${aluno}</td>
          <td><input type="checkbox" class="presenca" onchange="atualizarLinha(this)" checked /></td>
          <td><input type="text" class="justificativa" /></td>
          <td><input type="text" class="observacoes" /></td>
        `;
        frequenciaBody.appendChild(row);
        atualizarLinha(row.querySelector('.presenca'));
      });
    }

    function atualizarLinha(checkbox) {
      const row = checkbox.closest("tr");
      if (checkbox.checked) {
        row.classList.remove("faltou");
        row.classList.add("presente");
      } else {
        row.classList.remove("presente");
        row.classList.add("faltou");
      }
    }

    function gerarPDF() {
      const { jsPDF } = window.jspdf;
      const doc = new jsPDF({ unit: "mm", format: "a4" });

      // Coleta todos os dados do formulário
      const formData = {
        tipo: document.getElementById("tipo").value,
        responsavel: document.getElementById("responsavel").value,
        auxiliares: document.getElementById("auxiliares").value,
        leitura: document.getElementById("leitura").value,
        tema: document.getElementById("tema").value,
        data: formatarData(document.getElementById("data").value),
        conteudo: document.getElementById("conteudo").value,
        frequencia: Array.from(document.querySelectorAll("#frequencia tbody tr")).map(row => ({
          nome: row.cells[1].innerText,
          presente: row.cells[2].querySelector(".presenca").checked,
          justificativa: row.cells[3].querySelector(".justificativa").value || "-",
          observacao: row.cells[4].querySelector(".observacoes").value || "-"
        }))
      };

      // Configurações do PDF
      const margin = { left: 15, right: 15 };
      let y = 20;

      // Cabeçalho
      doc.setFontSize(14).setFont(undefined, "bold")
         .text("Diário de Catequese", margin.left, y);
      y += 7;
      
      doc.setFontSize(12)
         .text("Paróquia Nossa Senhora dos Remédios - Diocese de Petrolina", margin.left, y);
      y += 10;

      doc.setDrawColor(0).setLineWidth(0.5)
         .line(margin.left, y, 210 - margin.right, y);
      y += 10;

      // Informações básicas
      const infoFields = [
        { label: "Tipo de Catequese:", value: formData.tipo },
        { label: "Responsável:", value: formData.responsavel },
        { label: "Auxiliares:", value: formData.auxiliares, skipIfEmpty: true },
        { label: "Data:", value: formData.data },
        { label: "Leitura do Dia:", value: formData.leitura },
        { label: "Tema da Aula:", value: formData.tema }
      ];

      infoFields.forEach(field => {
        if (field.skipIfEmpty && !field.value) return;
        
        doc.setFont(undefined, "bold").text(field.label, margin.left, y);
        doc.setFont(undefined, "normal").text(field.value, margin.left + 40, y);
        y += 7;
      });

      y += 3;

      // Conteúdo trabalhado
      doc.setFont(undefined, "bold").text("Conteúdo Trabalhado:", margin.left, y);
      y += 7;
      
      const conteudoLines = doc.splitTextToSize(formData.conteudo, 180);
      conteudoLines.forEach(line => {
        doc.text(line, margin.left, y);
        y += 7;
      });
      y += 10;

      // Tabela de frequência
      doc.setFont(undefined, "bold").text("Frequência dos Alunos:", margin.left, y);
      y += 7;

      doc.autoTable({
        startY: y,
        head: [["Nº", "Nome", "Presença", "Justificativa", "Observações"]],
        body: formData.frequencia.map((item, index) => [
          index + 1,
          item.nome,
          { 
            content: item.presente ? "Presente" : "Faltou", 
            styles: { 
              fillColor: item.presente ? [200, 255, 200] : [255, 200, 200],
              textColor: [0, 0, 0]
            } 
          },
          item.justificativa,
          item.observacao
        ]),
        margin,
        headStyles: {
          fillColor: [70, 70, 70],
          textColor: [255, 255, 255],
          fontStyle: 'bold'
        },
        styles: {
          fontSize: 9,
          cellPadding: 3,
          overflow: 'linebreak'
        },
        didDrawPage: addFooter
      });

      // Nome do arquivo com data e turma
      const fileName = `Diario_Catequese_${formData.tipo.replace(/\s+/g, '_')}_${formData.data.replace(/\//g, '-')}.pdf`;
      doc.save(fileName);
    }

    function addFooter(doc) {
      doc.setFontSize(10).setTextColor(100)
         .text(
           `Gerado em ${new Date().toLocaleDateString('pt-BR')}`,
           doc.margin.left,
           doc.internal.pageSize.height - 10
         );
    }

    function formatarData(dataString) {
      if (!dataString) return "";
      const [year, month, day] = dataString.split('-');
      return `${day}/${month}/${year}`;
    }

    function limparSelecao() {
      // Limpa todos os campos do formulário
      document.querySelectorAll('input[type="text"], textarea').forEach(el => el.value = "");
      document.getElementById("data").value = "";
      document.querySelector("#frequencia tbody").innerHTML = "";
    }

    // Inicialização (pode ser útil para futuras expansões)
    document.addEventListener('DOMContentLoaded', function() {
      console.log('Diário de Catequese iniciado');
    });
  </script>
</body>
</html>
