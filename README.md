# CHANGE-MINING2025

<p align="center">
  <img src="imagem/20250719_1447_Logo CHANGE-MINING2025_simple_compose_01k0hwnqxre78sp04cw5pqkehk.png" alt="Logo CHANGE-MINING2025" width="250"/>
</p>


**CHANGE-MINING2025** é uma base de dados desenvolvida para tarefas de detecção de mudanças em áreas de mineração, com foco em aplicações de sensoriamento remoto e aprendizado profundo.

## 📦 Download

Você pode acessar e baixar a base de dados pelo link abaixo:

🔗 [Clique aqui para fazer o download da base CHANGE-MINING2025](https://drive.google.com/drive/folders/1QcCsCtugA8Gv_HTcdKiE7ePBfu21Ko7R?usp=sharing)


## 📂 Descrição da Base

A base é composta por pares bitemporais de imagens Sentinel-2, adquiridos em dois instantes de tempo distintos, com resolução espacial de 10 metros. As imagens são acompanhadas de máscaras binárias que indicam as regiões onde ocorreram mudanças associadas à atividade mineradora. Cada amostra contém:

- Uma imagem no tempo **T1** (ano de **2017**)
- Uma imagem no tempo **T2** (ano de **2024**)
- Uma **máscara binária de mudança**

## Estrutura da Base de Dados

A base de dados `CHANGE-MINING2025` está organizada da seguinte forma:


Cada amostra é composta por um par de imagens multiespectrais Sentinel-2 com resolução espacial de **10 metros**, capturadas em dois instantes distintos (**T1** e **T2**), além de uma **máscara binária** que identifica as áreas com indícios de **atividade mineradora** ao longo do tempo.

📁 **T1/**: Contém as imagens do primeiro instante de tempo (2017)  
📁 **T2/**: Contém as imagens do segundo instante de tempo (2024)  
📁 **Mudança/**: Máscaras binárias de referência (0 = sem mudança, 1 = mudança)



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
- Estudos de **uso e ocupação do solo** com foco em mineração

---

📌 *Para mais informações, consulte a publicação associada ou entre em contato com os autores do projeto.*
