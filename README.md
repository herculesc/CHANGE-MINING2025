# CHANGE-MINING2025

**CHANGE-MINING2025** é uma base de dados desenvolvida para tarefas de detecção de mudanças em áreas de mineração, com foco em aplicações de sensoriamento remoto e aprendizado profundo.

## 📂 Descrição da Base

A base é composta por imagens multitemporais provenientes do satélite Sentinel-2 e máscaras binárias que indicam as regiões onde ocorreram mudanças relacionadas à atividade mineradora. Cada amostra contém:

- Uma imagem no tempo **T1** (ano de **2017**)
- Uma imagem no tempo **T2** (ano de **2024**)
- Uma **máscara binária de mudança**

### 🗂️ Estrutura de Diretórios

CHANGE-MINING2025/
├── T1/ # Imagens do tempo inicial (2017)
├── T2/ # Imagens do tempo final (2024)
└── Mudança/ # Máscaras binárias de mudança (0 = sem mudança, 1 = mudança)


### 🛠️ Processo de Criação

O processo de elaboração da base envolveu as seguintes etapas:

1. **Aquisição das imagens** do Sentinel-2 através da plataforma [Copernicus Browser](https://browser.dataspace.copernicus.eu/).
2. **Seleção temporal** dos anos **2017 (T1)** e **2024 (T2)**, com cálculo do índice espectral **SAVI** para cada instante.
3. **Cálculo da mudança**, por meio da subtração dos índices SAVI (T2 - T1), seguido de **refinamento manual** das regiões alteradas.
4. **Geração da máscara de mudança**, com valores binários:
   - `0` = Sem alteração
   - `1` = Com alteração
5. **Recorte das imagens** em blocos de **128 × 128 pixels** utilizando o software **QGIS**.
6. **Organização final** da base nas três pastas: `T1/`, `T2/` e `Mudança/`.

## 🚀 Aplicações

A base de dados CHANGE-MINING2025 é ideal para:

- Modelos de **detecção de mudanças** com redes neurais profundas
- **Monitoramento ambiental** de áreas mineradas
- Estudos de **uso e ocupação do solo** com foco em mineração

---

📌 *Para mais informações, consulte a publicação associada ou entre em contato com os autores do projeto.*
