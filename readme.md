# VCFannotatoR 

#### Ferramenta para análise e anotação de variantes a partir de um arquivo VCF através do VEP ensembl 105.0

#### Utilizando o Google Colab

---


## As variantes são anotadas com as seguintes informações

> Tipo de variação anotada (substituição, inserção, CNV, etc.).

> Função (missense, silencioso, intergênico, etc.).

> Profundidade de leitura de sequência em cada local da variante.

> Número de leituras do alelo alternativo.

> Percentual de leituras que suportam o alelo alternativo contra aqueles que suportam o alelo de referência.

> Frequência de alelos das variantes pel VEP do Ensembl 105.0


---
Em um novo notebook no Google colab montar o drive

```
from google.colab import drive
drive.mount('/content/drive')
```
 ---
 
## Instalando VEP ensembl-vep-105.0

1. Instalar as dependências
2. Download da release ensembl-vep 105.0 no github
3. Descompactar o arquivo .tar.gz
4. Entrar no diretório
5. Rodar o script INSTALL.PL com a opção --NO_UPDATE (para não pegar a versão mais nova)

https://github.com/Ensembl/ensembl-vep/archive/refs/tags/105.0.tar.gz

```
%%bash
sudo apt install unzip curl git libmodule-build-perl libdbi-perl libdbd-mysql-perl build-essential zlib1g-dev
wget -c https://github.com/Ensembl/ensembl-vep/archive/refs/tags/105.0.tar.gz
tar -zxvf 105.0.tar.gz
cd ensembl-vep-105.0
./INSTALL.pl --NO_UPDATE
```

#### Teste do comando 

Testar a instalação do vep, executando o script ./vep
