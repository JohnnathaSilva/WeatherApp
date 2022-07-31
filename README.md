# WeatherApp
O aplicativo deve consumir a localização atual do usuário e exibir na interface o endereço atual e os dados climáticos da região

Casos de testes

--História<br />
Eu como usuário<br /> 
Quero realizar um cadastro no app<br /> 
Para compartilhar o clima do local em que me encontro<br /> 

--Funcionalidade<br />
Eu como usuário<br /> 
Quero compartilhar o clima do local em que me encontro<br /> 
Para que outros usuários possam visualizar essa informação<br /> 

--Casos de Testes

01 - Cadastrar informações climáticas com sucesso<br /> 
Dado que usuário está na página inicial do aplicativo<br /> 
Quando clicar no botão cadastro<br /> 
E informar telefone corretamente<br /> 
E informar corretamento o código de confirmação<br /> 
E informar nome corretamente<br /> 
E permitir acesso sua localização<br /> 
Então será exibido endereço atual e os dados climáticos da região<br /> 

02 - Visualizar informações do clima da região<br /> 
Dado que usuário está na página inicial do aplicativo<br /> 
Quando clicar no botão Entrar<br /> 
Então será exibido endereço atual e os dados climáticos da região<br /> 

03 - Cadastrar celular<br /> 
Dado que usuário inseriu um telefone válido<br /> 
Quando clicar em prosseguir<br /> 
Então será exibida a tela de Código de confirmação<br /> 

04 - Cadastrar celular inválido<br /> 
Dado que o usuário digitou um telefone inválido<br /> 
Quando clicar em prosseguir<br /> 
Então será exibida uma mensagem informando que o usuário deve digitar um telefone válido<br /> 

05 - Código de confirmação inválido<br /> 
Dado que usuário está na tela de Código de confirmação<br /> 
Quando digitar um código inválido<br /> 
Então será exibida a mensagem Código inválido. Tente novamente.<br /> 

06 - Reenvio de Código de confirmação<br /> 
Dado que usuário inseriu um telefone válido<br /> 
E está na tela de Código de confirmação<br /> 
Quando clicar no botão [REENVIE O CÓDIGO]<br /> 
Então será reenviado um novo código de corfirmação<br /> 

07 - Cadastro Nome<br /> 
Dado que usuário inseriu um nome válido<br /> 
Quando clicar em prosseguir<br /> 
Então será exibida a tela de compartilhar localização<br /> 

08 - Cadastrar nome inválido<br /> 
Dado que usuário inseriu um nome inválido<br /> 
Quando clicar em prosseguir<br /> 
Será exibida uma mensagem informando que é necessário inserir nome e sobrenome<br /> 

09 - Cadastrar Localização Permitir<br /> 
Dado que usuário clicou no botão [LOCALIZAÇÃO AUTOMÁTICA]<br /> 
Quando clicar em Sim<br /> 
Então será exibido endereço atual e os dados climáticos da região<br /> 

10 - Cadastrar Localização Recusar<br /> 
Dado que usuário clicou no botão [LOCALIZAÇÃO AUTOMÁTICA]<br /> 
Quando clicar em Não<br /> 
Então o usuário permanecerá na tela de cadastro de localização automática<br /> 
E será exibida a mensagem: é necessário permitir o acesso a localização atual para realizar o cadastro<br /> 

11 - Visualizar informações locais pelo horário<br /> 
Dado que o usuário se encontra na tela informações climáticas<br /> 
Quando alterar o horário<br /> 
Então será exibido o clima do horário selecionado<br /> 

12 - Visualizar informações locais pela data<br /> 
Dado que o usuário se encontra na tela informações climáticas<br /> 
Quando alterar a data<br /> 
Então será exibido o clima da data selecionada<br /> 


--Problemas<br />

//Tela Inicial<br /> 
01 - Sowe está com a letra W em lowercase<br /> 
02 - Cor da fonte errada do texto - android.widget.TextView - Saiba quantas pessoas próximas a você reportaram chuva e receba um aviso antes de sair de casa.<br /> 
03 - android.widget.TextView - Cadastrar e android.widget.TextView - Entrar estão sendo exibos muito abaixo na tela<br /> 
04 - Não há espaço entre a android.widget.TextView - Cadastrar e android.widget.TextView - Entrar<br /> 

//Cadastro Celular<br /> 
05 - Texto Cadastro que está sobrepondo a status bar - android.widget.TextView - Cadastro<br /> 
06 - Cor da fonte errada do texto - android.widget.TextView - Você receberá um código de confirmação no número de telefone celular informado.<br /> 
07 - É possível digitar qualquer caractere<br /> 
08 - Após inserir o telefone e prosseguir não é exibida a tela de código de confirmação<br /> 
09 - Ícone diferente do iOS android.widget.TextView - ><br /> 
10 - Máscara DD não é exibida<br /> 
11 - android.view.ViewGroup vai até o topo da tela quando o teclado virtual é acionado<br /> 

//Cadastro Nome<br />
12 - Divergência do app atual com o protótipo no campo Nome - Nome Completo (Atual)/ Nome (Protótipo)<br /> 
13 - TextView não exibe José Exemplo da Silva no android.widget.EditText<br /> 
14 - É possível cadastrar nome com apenas um espaço<br /> 
15 - Ícone diferente do iOS android.widget.TextView - ><br /> 

//Cadastro Localização<br /> 
16 - Cor da fonte errada do texto - android.widget.TextView - Para entregarmos informações mais precisas sobre o seu micro-clima, precisamos utilizar a sua localização automática.<br /> 
17 - Ícone dinâmico de um GPS não é exibido<br /> 

//Tela de informações climáticas<br /> 
18 - Sowe está com a letra W em lowercase<br /> 
19 - Ao clicar em Sair após realizar um cadastro ele volta pra tela de cadastro (Deveria volta para tela inicial)<br /> 
20 - Divergência do app atual com o protótipo - android.widget.TextView - CHANCE CH. (Atual)/ CHANC. CH (Protótipo)<br /> 
21 - Erros ortográfico android.widget.TextView - HUMIDADE / Correto UMIDADE<br /> 
22 - Erros ortográfico android.widget.TextView - JÁ É SENSASSÃO / Correto SENSAÇÃO<br /> 
23 - Data sendo exibida diferente do protótipo<br /> 
24 - Ao clicar na data ele solicita novamente a localização (Deveria ser aberto um calendário)<br /> 
25 - Não é possível selecionar horário<br /> 
26 - android.view.ViewGroup dos horários soobrepõe as informações do android.view.ViewGroup que exibe as inforção do clima (2340x1080 - Android 11 - Umidigi BISON PRO)<br /> 
27 - Em dispositivo que a android.view.ViewGroup dos horários é exibida o Endereço sobrepõe a status bar (1080 x 2340 - Android 13 - Pixel 5) e em dispostivos em que a android.view.ViewGroup dos horários não é exibida completamente não sobrepõe (2340x1080 - Android 11 - Umidigi BISON PRO)<br /> 
28 - Celular com baixa resolução não é possível visualizar nada após abrir o teclado virtual e na tela de informações climáticas várias informações não são exibidas (480 x 800 - Android 8 - Nexus S)<br /> 
29 - android.view.ViewGroup dos horários sobrepõe a android.view.ViewGroup informações climáticas (Tablet 2560 x 1800 - Android 13 - Pixel C)<br /> 
30 - Divergência do app atual com o protótipo - android.widget.TextView - Sair<br /> 


--Melhorias<br />
//Tela inicial<br /> 
01 - Alterar pra uma imagem com uma resolução maior - android.widget.ImageView<br /> 

//Cadastro Celular<br /> 
02 - Permitir inserir apenas números<br /> 
03 - Caso o usúario tente prosseguir sem informar os 11 números exibir uma mensagem informando que é necessário informar um número de telefone de 11 dígitos<br /> 

//Cadastro Nome<br /> 
04 - Caso o usúario tente prosseguir com apenas o primeiro nome exibir mensagem informando que é necessário informar nome e sobrenome<br /> 
05 - Limitar o número de caracteres que podem ser inseridos<br /> 

//Tela de informações climáticas<br /> 
06 - Adicionar um ScrollView em celulares que possuem uma baixa resolução 
<br /> 
