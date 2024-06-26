[![author](https://img.shields.io/badge/author-michaelcardoso-red.svg)](https://www.linkedin.com/in/michael-cardoso-84a9a0b2/)

# Áudio para Texto

   <p> Este projeto consiste em um programa de conversão de áudio para texto, utilizando a biblioteca <em>SpeechRecognition</em> do Python. <strong> O objetivo principal é fornecer uma ferramenta simples e eficiente para auxiliar na transcrição de arquivos de áudio em texto.</strong>
   
   ## Google Web Speech API

   O <em>SpeechRecognition</em> é uma biblioteca de Python que utiliza uma API de reconhecimento de fala para converter áudio em texto. O que é uma API? Uma API (Interface de Programação de Aplicativos), de modo simples, é um conjunto de regras e protocolos que permite que diferentes softwares se comuniquem entre si. É como uma ponte que permite que um programa utilize as funcionalidades de outro de maneira padronizada e organizada. Essa API, chamada de <em>Google Web Speech API</em>, é um serviço oferecido pela Google que faz o processamento da fala em tempo real e retorna o texto correspondente.
   
   A escolha dessa biblioteca se dá pela facilidade de uso: O <em>SpeechRecognition</em> é fácil de aprender e usar, o que torna a implementação do reconhecimento de fala em um programa Python bastante acessível, mesmo para desenvolvedores iniciantes. E também por ter suporte a várias APIs, populares de reconhecimento de fala, incluindo <em>Google Web Speech API</em>. Com recursos como o SpeechRecognition, os desenvolvedores podem incorporar funcionalidades de <strong>processamento de linguagem natural</strong> em suas aplicações, abrindo portas para interações mais intuitivas e acessíveis por meio da fala. 

   ## Como ocorre o processo?
   
   O funcionamento do <em>SpeechRecognition</em> com a API de reconhecimento de fala ocorre em etapas. Primeiro, o programa utiliza a biblioteca para ler um arquivo de áudio ou capturar áudio em tempo real. Em seguida, a biblioteca envia esse áudio para a API de reconhecimento de fala da Google. A API processa o áudio, utilizando algoritmos avançados de reconhecimento de fala, e retorna o texto correspondente.

   A biblioteca <em>SpeechRecognition</em> lida com toda a parte de comunicação com a API, tornando o processo transparente para o desenvolvedor. Ela fornece métodos simples para gravar áudio, enviar para a API e receber o texto reconhecido como resposta. Dessa forma, os desenvolvedores podem facilmente integrar o reconhecimento de fala em seus próprios programas, sem se preocupar com os detalhes complexos da API implícitos. A biblioteca facilita a comunicação com a API, permitindo que utilizemos o reconhecimento de fala em nossos programas de maneira simples e eficiente.
   
   ## Formato de áudio de entrada
   
   Neste projeto optamos pelo formato de arquivo de áudio WAV. Isto é, o programa aceitará apenas entrada de arquivos WAV.
   
   Em comparação com o o formato MP3, em WAV temos uma compressão sem perdas, a qualidade do som é superior ao MP3, sendo que o formato de arquivo WAV contém muitos detalhes de som, é maior e requer mais espaço. Porém, como desejamos a mais alta qualidade e não nos importamos com o tamanho do arquivo, escolhemos o formato WAV, muito utilizado por profissionais de áudio.
   
   ## Biblioteca utilizadas
   
   Fizemos uso das seguintes bibliotecas: PySimpleGUI; SpeechRecognition; Pydub; Docx; Time; e Datetime.
   Vamos comentar resumidamente a função de cada biblioteca que foi importada no projeto.

```python
import PySimpleGUI as sg
```
- `PySimpleGUI`: É uma biblioteca de interface gráfica que facilita a criação de interfaces de usuário (GUI) em Python. Ela fornece uma API simples e intuitiva para criar janelas, botões, caixas de entrada e outros elementos de interface.

```python
import speech_recognition as sr
```
- `speech_recognition`: É uma biblioteca que fornece recursos de reconhecimento de fala em Python. Ela permite capturar áudio de microfone ou arquivos de áudio e convertê-lo em texto utilizando serviços de reconhecimento de fala, como o Google Speech Recognition.

```python
from pydub import AudioSegment
```
- `pydub`: É uma biblioteca para manipulação de arquivos de áudio em Python. Ela oferece funcionalidades para carregar, cortar, mesclar, converter e reproduzir arquivos de áudio em vários formatos.

```python
from docx import Document
```
- `docx`: É uma biblioteca para criação e manipulação de documentos do Microsoft Word em Python. Ela permite criar, editar e salvar documentos .docx, além de fornecer recursos para adicionar texto, formatação, tabelas, imagens e outros elementos aos documentos.

```python
import time
```
- `time`: É um módulo que fornece funções relacionadas ao tempo, como medir a duração de um evento, adicionar atrasos ou pausas no programa e trabalhar com timestamps.

```python
import datetime
```
- `datetime`: É um módulo que fornece classes e funções para manipulação de datas e horas em Python. Ele permite obter informações sobre a data e hora atual, realizar cálculos de tempo, formatar datas e horas, entre outras operações relacionadas ao tempo.

Essas bibliotecas e módulos fornecem funcionalidades essenciais para o seu programa, como a criação da interface gráfica, reconhecimento de fala, manipulação de áudio e criação de documentos do Word.
   
   ## Descrição do Projeto
   
   Inicialmente pensou-se um programa que fosse simples e com poucas linhas de código. Assim, a primeira versão do programa acabou sendo desenvolvida para lidar com a conversão de pequenos trechos de áudio. Ela utiliza a função `recognize_google` da biblioteca <em>SpeechRecognition</em> para realizar a conversão de áudio em texto. Essa versão é adequada para transcrever áudios curtos, como mensagens de voz, anotações curtas ou pequenos trechos de diálogos. Embora seja simples, essa versão já pode ser útil para economizar tempo e esforço na trabalhosa transcrição manual.

   No entanto, como trabalhamos com realização de entrevistas com meia hora ou mais de gravação, percebemos a necessidade de uma versão mais robusta para lidar com a transcrição de áudios longos. A segunda versão do programa foi então desenvolvida para atender a essa nessecidade. Nessa versão, o áudio é dividido em pedaços de aproximadamente 30 segundos para evitar problemas de memória durante o processamento. Além do mais, foi realizada uma melhoria na precisão do reconhecimento de fala por meio do ajuste para o ruído ambiente antes de cada gravação. Daí a imporância de se realizar boas gravações, tentando se possível minimizar as interferências do som ambiente, pois a qualidade da gravação poderá influenciar no resultado final da impresssão do texto. Essa versão é capaz de transcrever áudios longos, como palestras, entrevistas, podcasts ou reuniões.

   A relevância desse tipo de programa é notável para pessoas que trabalham com a conversão manual de áudios para texto. Transcrever áudios manualmente pode ser um processo demorado e tedioso, exigindo muita atenção e esforço para ouvir cada frase e em seguida escrevê-las. Com o auxílio de um programa de conversão automática, como este, o trabalho é facilitado e acelerado, permitindo que as pessoas foquem em outras tarefas importantes.

   Em resumo, esse programa de conversão de áudio em texto é uma ferramenta valiosa para economizar tempo e esforço na transcrição manual. As duas versões, a primeira voltada para textos curtos e a segunda para textos longos, fornecem soluções específicas para diferentes necessidades. Através desse projeto, busca-se fornecer uma solução eficiente e acessível para melhorar a produtividade e facilitar a vida daqueles que precisam lidar com a transcrição de áudios.
   
   ### Lógica do programa step by step
   
   Por fim, falaremos da lógica do programa, detalhado o passo a passo de sua implementação. 
   
   A função main() é o ponto de entrada do programa. Quando o arquivo é executado diretamente (ou seja, não importado por outro módulo), a condição if __name__ == "__main__": é verdadeira e a função main() é chamada.
   
   Essa função é responsável por criar e exibir a janela da interface gráfica usando a biblioteca PySimpleGUI. Ela define o layout da janela, lida com os eventos dos botões e realiza as ações necessárias para converter um arquivo de áudio em texto.
   
   ### A função main() segue a seguinte lógica:
   
   * Configura a aparência da interface gráfica e exibe uma mensagem de boas-vindas.
   * Define o layout da janela com os elementos necessários, como um campo de entrada para o arquivo de áudio, botões de "Converter" e "Cancelar", uma barra de progresso e rótulos para exibir informações sobre o tempo decorrido e direitos autorais.
   * Entra em um loop principal para capturar e lidar com os eventos da janela.
   * Se o evento for o fechamento da janela (sg.WINDOW_CLOSED) ou o botão "Cancelar" for pressionado, o loop é interrompido e o programa é encerrado.
   * Se o evento for o botão "Converter" e um arquivo de áudio válido tiver sido selecionado, o programa continua com as etapas de conversão.
   * Carrega o arquivo de áudio usando a biblioteca AudioSegment do pydub.
   * Divide o áudio em partes de 30 segundos usando a função split_audio().
   * Inicia um loop para processar cada parte do áudio:
      * Exporta a parte atual como um arquivo WAV temporário.
      * Realiza a conversão de áudio para texto usando a função audio_to_text().
      * Atualiza a barra de progresso com base no progresso atual.
      * Atualiza o rótulo de tempo decorrido com base no tempo transcorrido desde o início da conversão.
      * Concatena o texto reconhecido em uma variável converted_text.
   * Cria um documento docx usando a biblioteca Document do python-docx.
   * Adiciona o texto reconhecido ao documento.
   * Exibe uma mensagem de conclusão da conversão.
   * Abre uma nova janela para definir o diretório e o nome do arquivo de texto a ser salvo.
   * Entra em um loop para capturar e lidar com os eventos da janela de salvamento.
   * Se o evento for o fechamento da janela ou o botão "Cancelar" for pressionado, o loop é interrompido e a janela de salvamento é fechada.
   * Se o evento for o botão "Salvar" e um diretório e nome de arquivo válidos forem fornecidos, o arquivo de texto é salvo.
   * Exibe uma mensagem informando se o arquivo foi salvo com sucesso ou exibe uma mensagem de erro se o diretório ou nome do arquivo forem inválidos.
   * Fecha a janela de salvamento.
   * Retorna ao loop principal para aguardar mais interações do usuário.
   
   Em resumo, a função main() é responsável por orquestrar a interface gráfica, o processamento de áudio e a conversão de áudio para texto, permitindo ao usuário selecionar um arquivo de áudio, acompanhando o progresso da conversão e salvando o texto convertido em um arquivo de texto.</p>
   
   <em>by Michael J M Cardoso</em>
   
   **Links:**
* [LinkedIn](https://www.linkedin.com/in/michael-cardoso-84a9a0b2/)
* [Medium](https://medium.com/@mjcursodatascience)
