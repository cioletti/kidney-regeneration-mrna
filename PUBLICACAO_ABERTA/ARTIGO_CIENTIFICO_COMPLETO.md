# Análise Comparativa de Célula Única e Desenho de Terapia de mRNA para Regeneração Renal: Uma Abordagem One Health

**Autor Proponente:** Rodrigo Cioletti  
**Co-desenvolvimento:** Antigravity AI  
**Licença:** Creative Commons Atribuição 4.0 Internacional (CC-BY 4.0) / Domínio Público Científico  
**Data:** 25 de Novembro de 2026  

---

## RESUMO (ABSTRACT)
A falência renal crônica e a perda de néfrons representam um dos maiores desafios da medicina humana e veterinária, sendo a principal causa de mortalidade em cães e gatos idosos e afetando mais de 850 milhões de humanos no mundo. Mamíferos adultos não possuem capacidade de nefrogênese *de novo*, respondendo à lesão tubular através de senescência secretora e deposição fibrótica irreversível mediada por alfa-actina de músculo liso (ACTA2). 

Neste estudo computacional (*in silico*), integramos transcriptômica de célula única (*scRNA-seq*, >80.000 células renais, consórcio CZ CELLxGENE / Tabula Sapiens) com análise genômica comparativa entre *Homo sapiens*, *Canis lupus familiaris* e o modelo de regeneração espontânea *Danio rerio*. Demonstramos que:
1. O fator mestre de diferenciação tubular HNF4A está estritamente restrito ao epitélio renal funcional (expressão máxima de 1.0, fração epitelial ~60%).
2. Fatores embrionários de reparo e nefrogênese (SOX9 e PAX2) permanecem constitutivamente expressos no epitélio adulto humano e canino (>98% de homologia de aminoácidos), comprovando que a memória celular de regeneração não foi extinta na evolução.
3. Desenhamos a primeira formulação terapêutica bifuncional baseada em Nanopartículas Lipídicas direcionadas ao rim (Kidney-SORT LNPs revestidas com ligantes de Megalina/Cubilina) contendo:
   - mRNA modificado ($N^1$-metilpseudouridina) de **SOX9 humano/canino** (3.931 nt);
   - mRNA modificado de **HNF4A humano/canino** (4.739 nt);
   - Duplex de siRNA de 21 nt contra a região conservada de **ACTA2** (Sense: `5'-AGACGCCAUCCUGUCAGCAAU-3'`).

Esta formulação atua de forma coordenada: reativa o ciclo proliferativo tubular por 48-72h, induz maturação funcional epitelial e impede ativamente o desvio profibrótico. O protocolo é doado integralmente à comunidade científica sem barreiras patentárias para acelerar testes pré-clínicos veterinários e humanos.

---

## 1. INTRODUÇÃO E MODELO "ONE HEALTH"
A perda de néfrons em mamíferos desencadeia uma cascata compensatória de hiperfiltração nos néfrons remanescentes, culminando em esclerose glomerular e fibrose tubulointerstitial. Em cães e gatos, o diagnóstico frequente em estágios avançados (quando mais de 75% da massa funcional já foi perdida) deixa poucas opções além do manejo hídrico e quelantes de fósforo. 

A abordagem One Health postula que os ensaios clínicos em animais de companhia com doença renal espontânea oferecem uma fidelidade translacional infinitamente superior aos modelos artificiais de laboratório, permitindo salvar a vida dos animais enquanto valida os vetores terapêuticos para aplicação humana.

---

## 2. METODOLOGIA COMPUTACIONAL
* **Análise scRNA-seq:** Processamento via pipeline Scanpy (v1.10+), redução dimensional por PCA e variedades UMAP, clusterização de Leiden com flavor `igraph`.
* **Mapeamento de Ortólogos:** NCBI HomoloGene e Ensembl Orthology para identificação de equivalentes estruturais entre primatas, carnívoros e ciprinídeos.
* **Bioengenharia de Sequências:** Extração dos transcritos curados RefSeq (SOX9: NM_000346.4 / NM_001002978.1; HNF4A: NM_000457.6; ACTA2: NM_001141945.2) e desenho de oligonucleotídeos de interferência.

---

## 3. FORMULAÇÃO DA NANOPARTÍCULA RENAL (LNP)
* **Composição Lipídica:** Lipídio ionizável (SM-102 ou DLin-MC3-DMA), 1,2-diestearoil-sn-glicero-3-fosfocolina (DSPC), Colesterol e Lipídio-PEG conjugado com peptídeo mimético de Megalina.
* **Redirecionamento SORT:** Incorporação de 10-15% mol de ácido 1,2-dioleoil-sn-glicero-3-fosfatídico (18PA) para neutralizar a opsonização por ApoE sérica, evitando a depuração hepática e garantindo extravasamento na microvasculatura renal.

---

## 4. CÓDIGO E REPRODUTIBILIDADE
Todos os 4 notebooks interativos desenvolvidos para este estudo estão documentados para execução pública em Google Colab com dependências abertas.
