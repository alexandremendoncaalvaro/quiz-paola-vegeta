# Quiz: Paola Bracho vs Vegeta - Quem disse?

Um quiz divertido para adivinhar se uma frase foi dita por Paola Bracho (da novela "A Usurpadora") ou por Vegeta (de Dragon Ball Z).

## Como Usar

### Requisitos

- Um servidor web local (não funciona abrindo diretamente o arquivo HTML)
- Navegador moderno com suporte a JavaScript ES6+

### Iniciando o Quiz

1. Clone ou baixe este repositório
2. Inicie um servidor web local no diretório:
   ```bash
   # Python 3
   python3 -m http.server 8080
   
   # Python 2
   python -m SimpleHTTPServer 8080
   
   # Node.js (se tiver npx)
   npx http-server -p 8080
   
   # PHP
   php -S localhost:8080
   ```
3. Abra o navegador em `http://localhost:8080/index.html`

### Como Jogar

1. Clique em **"Próxima"** para ver uma frase
2. Escolha quem disse: **Paola Bracho** ou **Vegeta**
3. No modo difícil, use **"Próxima"** para continuar (ou ative o modo estudo)
4. Use **"Recomeçar"** para resetar o placar

#### Atalhos de Teclado
- `N` - Próxima pergunta
- `R` - Recomeçar
- `1` - Selecionar Paola Bracho
- `2` - Selecionar Vegeta

#### Modos de Jogo

- **Modo Difícil**: Não revela a resposta automaticamente
- **Modo Casual**: Mostra a resposta após cada escolha
- **Modo Estudo**: Mostra fonte e autor após responder
- **Evitar óbvias**: Remove frases muito fáceis
- **Só cruéis/sarcásticas**: Apenas frases sem violência gráfica

## Como Adicionar Novas Frases

As frases ficam no arquivo `phrases.json`. Para adicionar novas:

1. Abra o arquivo `phrases.json`
2. Adicione um novo objeto no array seguindo este formato:

```json
{
  "id": "P09",
  "who": "Paola",
  "cruel": true,
  "obvious": false,
  "text": "Sua nova frase aqui",
  "src": "Fonte da frase (episódio, compilação, etc)"
}
```

### Campos Explicados

- **id**: Identificador único (P01, P02... para Paola; V01, V02... para Vegeta)
- **who**: `"Paola"` ou `"Vegeta"`
- **cruel**: `true` se a frase é cruel/sarcástica, `false` se não
- **obvious**: `true` se a frase é muito óbvia, `false` se não
- **text**: O texto da frase
- **src**: Fonte onde a frase foi encontrada

### Exemplo Completo

```json
[
  {
    "id": "P01",
    "who": "Paola",
    "cruel": true,
    "obvious": false,
    "text": "Sempre há uma testemunha perigosa de suas maldades... mas os mortos não falam.",
    "src": "UOL/YouTube/Pensador (compilações)"
  },
  {
    "id": "V01",
    "who": "Vegeta",
    "cruel": true,
    "obvious": false,
    "text": "Kakarotto imundo, roubarei o dinheiro daquele verme insolente para me alimentar!",
    "src": "Wikiquote (PT)"
  }
]
```

### Dicas

- Certifique-se de que o JSON está válido (pode usar [jsonlint.com](https://jsonlint.com))
- Mantenha o balanceamento entre frases de Paola e Vegeta
- Evite adicionar vírgula após o último item do array
- Teste no navegador após adicionar novas frases

## Estrutura do Projeto

```
.
├── index.html      # Aplicação principal (HTML + CSS + JavaScript)
├── phrases.json    # Banco de dados de frases
└── README.md       # Este arquivo
```

## Tecnologias

- HTML5
- CSS3 (design dark mode)
- JavaScript ES6+ (Fetch API, async/await)

## Créditos

Frases coletadas de compilações públicas disponíveis em:
- UOL
- Terra
- YouTube
- Pensador
- Wikiquote (PT)

---

Divirta-se jogando! 🎮
