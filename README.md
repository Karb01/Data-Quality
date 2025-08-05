# 🧪 Data Quality Validator

Valide automaticamente a qualidade de arquivos `.xlsx` (Excel) aplicando regras de negócio e estrutura.

---

## 📂 Estrutura do Projeto

```
Data_Quality/
├── Main_Data_Quality.py             # Script principal: executa todas as validações
├── ManipulaArquivo.py               # Carrega e move arquivos
├── Valida_Bac.py                    # Valida campo BAC
├── Valida_Campos_Obrigatorios.py    # Verifica campos essenciais
├── Valida_Colunas_Novas.py          # Detecta colunas inesperadas
├── Valida_ddi_telefone.py           # Valida DDI vs. telefone
├── Valida_Duplicatas.py             # Identifica duplicatas
├── Valida_Nota.py                   # Valida notas
├── Processados/                     # Arquivos já processados
└── README.md                        # Este arquivo
```

---

## ⚙️ Como usar

1. Coloque os arquivos `.xlsx` na pasta `Data_Quality`.
2. Execute:

   ```bash
   python Main_Data_Quality.py
   ```

3. O sistema:
   - Carrega o primeiro arquivo Excel encontrado
   - Executa todas as validações
   - Imprime os resultados
   - Move o arquivo para `Processados/`

---

## ✅ Regras de Validação

- **BAC**: Apenas números, até 6 dígitos.
- **Campos obrigatórios**: Ex: VIN, CPF, STATUS.
- **Colunas novas**: Sinalizadas se não esperadas.
- **DDI vs. Telefone**: Confere coerência.
- **Duplicatas**: Linhas repetidas.
- **Notas**: Entre 0 e 10, sem negativos.

---

## 🛠️ Requisitos

- Python 3.10+
- Bibliotecas:
  - pandas
  - numpy
  - openpyxl

Instale com:

```bash
pip install -r requirements.txt
```

Crie o arquivo `requirements.txt`:

```txt
pandas
numpy
openpyxl
```

---

## 🧼 .gitignore

Inclua:

```gitignore
__pycache__/
*.pyc
*.xlsx
Processados/
```
---

## 📄 Licença

MIT License. Veja o arquivo [LICENSE](LICENSE).
