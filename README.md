**# AED3-TP03**  
**Backup compactado**

Dado o código utilizado na realização do TP2 e a classe `LZW`, estas foram as mudanças feitas:

Adição do arquivo **MenuBackUps**:

1. Adicionamos um menu com as opções de criar um BackUp ou carregar um BackUp antigo.
2. Chamamos as funções do **Compactador** por meio das funções do menu `fazerBackup` e `carregarBackup` para realizar a compactação dos dados atuais ou os recuperar.

Adição do arquivo **Compactador**:

1. Criamos a classe Compactador onde fazemos as rotinas de compressão dos dados em arquivos de BackUp e de descompressão destes dados de volta para a pasta dados.
2. Criamos a função `compacta`, que percorre o diretório de dados lendo todos os arquivos e armazenando no arquivo de BackUp o nome do arquivo em bytes, indicador de tamanho dos dados comprimidos e o arquivo comprimido.
3. Dentro da função `compacta` o método `codifica` do LZW é chamado uma vez para arquivo no diretório de dados.
4. Criamos a função `descompacta`, que recebe a versão do BackUp a ser recuperado. A função lê o nome do arquivo, o tamanho dos dados compactados e o prório array de bytes, e cria na pasta de dados o arquivo com o nome recuperado e escreve no mesmo os dados após serem descompactados.
5. Dentro da função `descompacta` o método `decodifica` do LZW é chamado uma vez para arquivo salvo no BackUp.

**Observações**:
- O sistema guarda apenas um BackUp por dia

**Nossa experiência fazendo**: Conseguimos fazer o trabalho implementando tudo que foi pedido, não foi uma atividade complexa de se entender o problema e nem tão difícil de se implementar. Eu (Gustavo Garcia) tive um problema para conseguir fazer o método de descompressão corretamente, mas depois de algum tempo consegui entender a implementação.

**Questionário**
* Foi feita uma rotina de compactação utilizando o algorítimo do LZW para fazer o backup dos arquivos

* Foi feita uma rotina de descompactação utilizando o algorítimo do LZW para recuperar o backup dos arquivos

* O usuário pode escolher qual versão recuperar

* Conseguimos uma taxa de aproximadamente 69% de compressão (0,69801145938658577687900235928547)

* O trabalho funciona corretamente 

* O trabalho está completo 

* O trabalho não é cópia 
