# WeatherApp
O aplicativo deve consumir a localização atual do usuário e exibir na interface o endereço atual e os dados climáticos da região

Casos de testes

--História
Eu como usuário
Quero realizar um cadastro no app
Para compartilhar o clima do local em que me encontro

--Funcionalidade
Eu como usuário
Quero compartilhar o clima do local em que me encontro
Para que outros usuários possam visualizar essa informação

--Casos de Testes

01 - Cadastrar informações climáticas com sucesso
Dado que usuário está na página inicial do aplicativo
Quando clicar no botão cadastro
E informar telefone corretamente
E informar corretamento o código de confirmação
E informar nome corretamente
E permitir acesso sua localização
Então será exibido endereço atual e os dados climáticos da região

02 - Visualizar informações do clima da região
Dado que usuário está na página inicial do aplicativo
Quando clicar no botão Entrar
Então será exibido endereço atual e os dados climáticos da região

03 - Cadastrar celular
Dado que usuário inseriu um telefone válido
Quando clicar em prosseguir
Então será exibida a tela de Código de confirmação

04 - Cadastrar celular inválido
Dado que o usuário digitou um telefone inválido
Quando clicar em prosseguir
Então será exibida uma mensagem informando que o usuário deve digitar um telefone válido

05 - Código de confirmação inválido
Dado que usuário está na tela de Código de confirmação
Quando digitar um código inválido
Então será exibida a mensagem Código inválido. Tente novamente.

06 - Reenvio de Código de confirmação
Dado que usuário inseriu um telefone válido
E está na tela de Código de confirmação
Quando clicar no botão [REENVIE O CÓDIGO]
Então será reenviado um novo código de corfirmação

07 - Cadastro Nome
Dado que usuário inseriu um nome válido
Quando clicar em prosseguir
Então será exibida a tela de compartilhar localização

08 - Cadastrar nome inválido
Dado que usuário inseriu um nome inválido
Quando clicar em prosseguir
Será exibida uma mensagem informando que é necessário inserir nome e sobrenome

09 - Cadastrar Localização Permitir
Dado que usuário clicou no botão [LOCALIZAÇÃO AUTOMÁTICA]
Quando clicar em Sim
Então será exibido endereço atual e os dados climáticos da região

10 - Cadastrar Localização Recusar
Dado que usuário clicou no botão [LOCALIZAÇÃO AUTOMÁTICA]
Quando clicar em Não
Então o usuário permanecerá na tela de cadastro de localização automática
E será exibida a mensagem: é necessário permitir o acesso a localização atual para realizar o cadastro

11 - Visualizar informações locais pelo horário
Dado que o usuário se encontra na tela informações climáticas
Quando alterar o horário
Então será exibido o clima do horário selecionado

12 - Visualizar informações locais pela data
Dado que o usuário se encontra na tela informações climáticas
Quando alterar a data
Então será exibido o clima da data selecionada


--Problemas
//Tela Inicial
01 - Sowe está com a letra W em lowercase
02 - Cor da fonte errada do texto - android.widget.TextView - Saiba quantas pessoas próximas a você reportaram chuva e receba um aviso antes de sair de casa.
03 - android.widget.TextView - Cadastrar e android.widget.TextView - Entrar estão sendo exibos muito abaixo na tela
04 - Não há espaço entre a android.widget.TextView - Cadastrar e android.widget.TextView - Entrar

//Cadastro Celular
05 - Texto Cadastro que está sobrepondo a status bar - android.widget.TextView - Cadastro
06 - Cor da fonte errada do texto - android.widget.TextView - Você receberá um código de confirmação no número de telefone celular informado.
07 - É possível digitar qualquer caractere
08 - Após inserir o telefone e prosseguir não é exibida a tela de código de confirmação
09 - Ícone diferente do iOS android.widget.TextView - >
10 - Máscara DD não é exibida
11 - android.view.ViewGroup vai até o topo da tela quando o teclado virtual é acionado

//Cadastro Nome
12 - Divergência do app atual com o protótipo no campo Nome - Nome Completo (Atual)/ Nome (Protótipo)v 
13 - TextView não exibe José Exemplo da Silva no android.widget.EditText
14 - É possível cadastrar nome com apenas um espaço
15 - Ícone diferente do iOS android.widget.TextView - >

//Cadastro Localização
16 - Cor da fonte errada do texto - android.widget.TextView - Para entregarmos informações mais precisas sobre o seu micro-clima, precisamos utilizar a sua localização automática.
17 - Ícone dinâmico de um GPS não é exibido

//Tela de informações climáticas
18 - Sowe está com a letra W em lowercase
19 - Ao clicar em Sair após realizar um cadastro ele volta pra tela de cadastro (Deveria volta para tela inicial)
20 - Divergência do app atual com o protótipo - android.widget.TextView - CHANCE CH. (Atual)/ CHANC. CH (Protótipo)
21 - Erros ortográfico android.widget.TextView - HUMIDADE / Correto UMIDADE
22 - Erros ortográfico android.widget.TextView - JÁ É SENSASSÃO / Correto SENSAÇÃO
23 - Data sendo exibida diferente do protótipo
24 - Ao clicar na data ele solicita novamente a localização (Deveria ser aberto um calendário)
25 - Não é possível selecionar horário
26 - android.view.ViewGroup dos horários soobrepõe as informações do android.view.ViewGroup que exibe as inforção do clima (2340x1080 - Android 11 - Umidigi BISON PRO)
27 - Em dispositivo que a android.view.ViewGroup dos horários é exibida o Endereço sobrepõe a status bar (1080 x 2340 - Android 13 - Pixel 5) e em dispostivos em que a android.view.ViewGroup dos horários não é exibida completamente não sobrepõe (2340x1080 - Android 11 - Umidigi BISON PRO)
28 - Celular com baixa resolução não é possível visualizar nada após abrir o teclado virtual e na tela de informações climáticas várias informações não são exibidas (480 x 800 - Android 8 - Nexus S)
29 - android.view.ViewGroup dos horários sobrepõe a android.view.ViewGroup informações climáticas (Tablet 2560 x 1800 - Android 13 - Pixel C)
30 - Divergência do app atual com o protótipo - android.widget.TextView - Sair


--Melhorias
//Tela inicial
01 - Alterar pra uma imagem com uma resolução maior - android.widget.ImageView

//Cadastro Celular
02 - Permitir inserir apenas números
03 - Caso o usúario tente prosseguir sem informar os 11 números exibir uma mensagem informando que é necessário informar um número de telefone de 11 dígitos

//Cadastro Nome
04 - Caso o usúario tente prosseguir com apenas o primeiro nome exibir mensagem informando que é necessário informar nome e sobrenome
05 - Limitar o número de caracteres que podem ser inseridos

//Tela de informações climáticas
06 - Adicionar um ScrollView em celulares que possuem uma baixa resolução
