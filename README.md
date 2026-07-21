# BluDialogBox

BluDialogBox é uma biblioteca em Go baseada no **Fyne** que fornece **caixas de diálogo prontas e reutilizáveis** para aplicações desktop, como alertas, confirmações e seleção de arquivos ou diretórios.

O objetivo é simplificar a criação de diálogos comuns, mantendo uma API limpa, consistente e fácil de integrar.

---

## ✨ Recursos

* Alertas simples (informação/erro)
* Caixa de confirmação com múltiplos botões
* Abertura de arquivos (com filtro de extensões)
* Salvamento de arquivos
* Seleção de diretórios
* Suporte a seleção múltipla
* Callbacks para retorno de ações do usuário

---

## 📦 Instalação

```bash
go get github.com/bluiceoficial/bludialogbox
```

---

## 🚀 Uso

### 🔔 Alerta

```go
bludialogbox.NewAlert(
	app,
	"Aviso",
	"Operação concluída com sucesso",
	false,
	"OK",
)
```

---

### ❓ Confirmação com múltiplos botões

```go
bludialogbox.NewConfirm(
	app,
	"Confirmação",
	"Deseja continuar?",
	[]string{"Sim", "Não", "Cancelar"},
	func(result int) {
		// result começa em 0 (Sim = 0, Não = 1, Cancelar = 2)
	},
)
```

---

### 📂 Abrir arquivo

```go
bludialogbox.NewOpenFile(
	app,
	"Abrir Arquivo",
	[]string{"png", "jpg", "pdf"},
	false,
	func(files []string) {
		// arquivos selecionados
	},
)
```

---

### 💾 Salvar arquivo

```go
bludialogbox.NewSaveFile(
	app,
	"Salvar Arquivo",
	[]string{"txt", "md"},
	func(path string) {
		// caminho escolhido
	},
)
```

---

### 📁 Selecionar diretório

```go
bludialogbox.NewSelectDirectory(
	app,
	"Selecionar Pasta",
	true,
	func(paths []string) {
		// diretórios selecionados
	},
)
```

---

## 👤 Autor

**Murilo Gomes Julio**

🔗 [https://www.bluice.com.br](www.bluice.com.br)

📺 [https://youtube.com/@bluiceoficial](https://youtube.com/@bluiceoficial)

---

## License

Copyright (c) 2026 Murilo Gomes Julio

Licensed under the [MIT](https://github.com/bluiceoficial/bludialogbox/blob/main/LICENSE) license.

All contributions to the BluDialogBox are subject to this license.