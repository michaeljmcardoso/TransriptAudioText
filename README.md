# Áudio para Texto
Programa que transcreve um arquivo de áudio para texto no Python.
Veja como é fácil transcrever áudio para texto com algumas linhas de código, utilizando API do google Speech Recognition.

Este projeto consiste em um programa de conversão de áudio em texto utilizando a biblioteca **SpeechRecognition em Python**. O objetivo principal é **fornecer uma ferramenta simples e eficiente para auxiliar na transcrição de áudios para texto**.

A primeira versão do programa foi desenvolvida para lidar com a conversão de pequenos trechos de áudio. Ela utiliza a função recognize_google da biblioteca SpeechRecognition para realizar a conversão de áudio em texto. Essa versão é adequada para transcrever áudios curtos, como mensagens de voz, anotações rápidas ou pequenos trechos de diálogos. Embora seja simples, essa versão já pode ser útil para economizar tempo e esforço na transcrição manual.

No entanto, percebeu-se a necessidade de uma versão mais robusta para lidar com a transcrição de áudios longos. A segunda versão foi então desenvolvida para atender a essa demanda. Nessa versão, o áudio é dividido em partes de aproximadamente 30 segundos para evitar problemas de memória durante o processamento. Além disso, é realizada uma melhoria na precisão do reconhecimento de fala através do ajuste para o ruído ambiente antes de cada gravação. Essa versão é capaz de transcrever áudios longos, como palestras, entrevistas, podcasts ou reuniões.

A relevância desse tipo de programa é notável para pessoas que trabalham com a conversão manual de áudios para texto. Transcrever áudios manualmente pode ser um processo demorado e tedioso, exigindo muita atenção e esforço. Com o auxílio de um programa de conversão automática, como este, o trabalho é facilitado e acelerado, permitindo que as pessoas foquem em outras tarefas importantes. Além disso, o programa pode ajudar pessoas com deficiência auditiva ao converter áudios em tempo real, facilitando a compreensão e comunicação.

Em resumo, esse programa de conversão de áudio em texto é uma ferramenta valiosa para economizar tempo e esforço na transcrição manual. As duas versões, a primeira voltada para textos curtos e a segunda para textos longos, fornecem soluções específicas para diferentes necessidades. Através desse projeto, busca-se fornecer uma solução eficiente e acessível para melhorar a produtividade e facilitar a vida daqueles que precisam lidar com a transcrição de áudios.
