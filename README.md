# 🏠 Cadastro de Endereço com CEP

Um app bem tranquilo feito em React que busca seus dados de endereço automaticamente só digitando o CEP. A aplicação tira toda a informação tediosa de preencher formulário consultando a API pública do [ViaCEP](https://viacep.com.br).

## ✨ O que funciona aqui

- 🔍 Busca o endereço automaticamente assim que você termina de digitar o CEP (8 dígitos)
- 📝 Preenche rua, bairro, cidade e estado automáticamente
- 🎭 Formata o CEP com máscara visual `00000-000` enquanto você digita
- ❌ Mostra erro amigável quando o CEP é inválido ou não existe
- ⚡ Cancela requisições antigas pra não ficar exibindo dados desatualizados

## 🛠️ Tecnologias

- [React 18](https://react.dev) + [Vite](https://vitejs.dev) — fast na live dev
- `fetch` nativo, zero dependências de rede

## 🚀 Como rodar

```bash
npm install
npm run dev      # roda em modo desenvolvimento (http://localhost:5173)
npm run build    # cria a versão de produção em dist/
npm run preview  # testa o build de produção localmente
```

## 📁 Organização do código

```
src/
  App.jsx              # componente principal com o formulário
  main.jsx             # entry point do React
  index.css            # estilos da aplicação
  services/viaCep.js   # camada da API (separada da UI)
```

## 💻 Como usar

1. Digite um CEP com 8 dígitos (ex: `01310100`)
2. A máscara visual formata automaticamente: `01310-100`
3. Assim que completa, a busca acontece e os campos se preenchem
4. Se o CEP não existir, aparece um aviso vermelho
5. Você pode editar qualquer campo manualmente depois se precisar
