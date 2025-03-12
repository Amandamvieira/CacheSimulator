#🚀 Cache Simulator

Este projeto é um simulador de cache desenvolvido em Python, que permite a configuração de diferentes parâmetros para simular o comportamento da cache em sistemas computacionais.


Random (R)

FIFO (F - First In, First Out)

LRU (L - Least Recently Used)

LRU Approximation (A - Algoritmo de substituição baseado em clock)

Entrada de dados via arquivos binários contendo endereços de memória

Geração de estatísticas detalhadas sobre os acessos à cache

🛠️ Como executar

1️⃣ Instale as dependências

Este projeto utiliza NumPy. Para instalar, execute:

pip install numpy

2️⃣ Faça o upload do arquivo de entrada

Os endereços de memória devem estar em um arquivo binário. No Google Colab, faça o upload manualmente ou utilize:

from google.colab import files
uploaded = files.upload()

3️⃣ Execute o simulador

No Google Colab ou terminal, execute:

python cache_simulator.py

Caso esteja no Google Colab, basta rodar o script diretamente após definir o caminho do arquivo binário.

⚙️ Configuração da Cache

Você pode configurar os seguintes parâmetros diretamente no código:

nsets = 256       # Número de conjuntos na cache
bsize = 4         # Tamanho do bloco em bytes
assoc = 1         # Grau de associatividade (1 = mapeamento direto)
subst = "R"       # Política de substituição (R, F, L, A)
flag_saida = 1    # Formato da saída (0 = detalhado, 1 = compacto)
arquivo_entrada = "/content/bin_1000.bin"  # Caminho do arquivo binário

📊 Formato da saída

O simulador gera estatísticas como:

Número total de acessos

Taxa de hits e misses

Misses por categoria: compulsório, capacidade e conflito

Exemplo de saída (modo compacto flag_saida = 1):

100000 0.92 0.08 1.00 0.00 0.00

Exemplo de saída (modo detalhado flag_saida = 0):

Número de acessos: 100000
Taxa de hits: 0.92   Número de hits: 92000
Taxa de misses: 0.08 Número de misses: 8000

📂 Estrutura do Projeto

📁 CacheSimulator/
│-- cache_simulator.py  # Código principal do simulador
│-- README.md           # Documentação do projeto
│-- bin_1000.bin        # Exemplo de arquivo de entrada

📜 Licença

Este trabalho foi desenvolvido pelas alunas Amanda e Eduarda como parte de um estudo sobre simulação de cache.

Este projeto é de código aberto e pode ser modificado livremente.
