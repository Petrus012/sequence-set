# 🗂️ Sequence Set em C++

Implementação da estrutura **Sequence Set** em C++: os registros de um arquivo CSV são convertidos para um arquivo binário organizado em blocos ordenados por ID, e o programa permite inserir, remover, buscar e listar registros diretamente no arquivo.

Trabalho acadêmico da disciplina de Indexação em Sistemas de Informação, na UFLA. A base de dados usada é um recorte público de estatísticas de transferência de imóveis da Nova Zelândia.

## ✨ Funcionalidades

- Conversão do CSV para arquivo binário organizado em blocos
- Inserção de registros, sem permitir IDs duplicados
- Remoção e busca de registros pelo ID
- Listagem de todos os registros armazenados

## 🔑 Como funciona

- **Blocos:** cada bloco guarda até 100 registros. Quando a capacidade do arquivo é excedida, um novo arquivo binário é criado (`data2.bin`).
- **Ordenação:** cada bloco é mantido ordenado por `id` com Insertion Sort.
- **Acesso em disco:** leitura e gravação binárias, com registros de tamanho fixo.
- **Remoção:** os registros restantes são regravados em um arquivo temporário, que substitui o original.
- **Erros tratados:** falha na abertura de arquivos e tentativa de inserir ID já existente.

## 🚀 Como executar

Pré-requisito: compilador C++11 ou superior (GCC, MinGW ou MSVC).

```bash
git clone https://github.com/Petrus012/sequence-set.git
cd sequence-set
g++ -o SequenceSet PROJETO_FINAL.cpp
./SequenceSet
```

Na primeira execução, o arquivo `dadosSequenceSet_id.csv` é convertido automaticamente para `data.bin`.

### Menu

```text
1. Inserir dado
2. Remover dado
3. Buscar dado
4. Sair
5. Imprimir todos os dados
```

## 📂 Estrutura

```text
.
├── PROJETO_FINAL.cpp         # código-fonte
├── dadosSequenceSet_id.csv   # base de dados de entrada
└── README.md
```

## 👥 Autores

- **Pyêtro Augusto Malaquias** ([@Petrus012](https://github.com/Petrus012))
- **João Vitor Givisiez Lessa** ([@joao-givisiez](https://github.com/joao-givisiez))
