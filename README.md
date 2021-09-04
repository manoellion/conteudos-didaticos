<!DOCTYPE html>
<html lang="pt">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>processadores</title>
    <style>
        body {
            background-color: darkslategray;
            margin: 10%;
            text-align: justify;
            padding: 5%;
            border-style: solid;
        }

        h1,
        h2,
        h3 {
            text-align: center;
            text-transform: capitalize;
        }

        table ,td{
            border-style: solid;
            font-size: 18px;
        }
        p,li{
            font-size: 18px;
            font-family: Arial, Helvetica, sans-serif;
        }
        a:visited{
            color: brown;
        }
        a:link{
            color: rgb(231, 216, 216);
        }
        a:hover{
            color: forestgreen;
        }
        a:active{
            color: red;
        }
        ul{
            list-style: none;
        }
    </style>
</head>

<body>
    <header id="inicio">
        <nav>
            <ul>
                <li><a href="#a">cada processo possui</a></li>
                <li><a href="#b">tabela de processos</a></li>
                <li><a href="#c">estados de um processo</a></li>
            </ul>
        </nav>
    </header>
    <h1>processo</h1>
    <p>
        definição: um processo é carectrizado por um programa em execução.
    </p>
    <p>
        a diferença de um programa por um processo: um processo é uma intancia de um programa e possui dados de entrada
        de saida e um estado (execuntando, bloqueado, pronto.)
    </p>
    <h2>processo em primeiro plano</h2>
    <ol>
        <li> interage com o usuario</li>
        <ul>
            <li> ler um arquivo</li>
            <li> iniciar um programa (linha de comando ou um duplo clique no mouse)</li>
        </ul>
    </ol>
    <h2>processo em segundo plano</h2>
    <p>
        processo com funções específicas(background) que independem (não interage com usuario) de
        usuarios-deamons:<br>1)recepção<br>2)serviços de impressão
    </p>
    <h2 id="a">cada processo possui</h2>
    <ol>
        <li><b>conjunto de instruções</b></li>
        <li><B>espaço de endereçamento</B> espaço reservado para que o processo possa ler e escrever</li>
        <li><b>contexto de hardware</b> valores no registradores, como PC, ponterio de pilha e ref. de porp. gerais</li>
        <li><b>contexto de software</b> atributos em geral, como lista de aquivos abertos, variaveis, etc. </li>
    </ol>
    <a href="#inicio">volte ao inicio</a>
    <h2>espaço de endereçamento</h2>
    <ol>
        <li><b>texto:</b>codigo executavel do(s) programa(s)</li>
        <li><b>dados:</b> as variaveis</li>
        <li><b>pilha de execução:</b></li>
        <ul>
            <li>controle a execução do processo</li>
            <li>empilhamento chamadas a procedimento, seus parametros e variaveis locais, etc.</li>
        </ul>
    </ol>
    <h2 id="b"> tabela de processos</h2>
    <table>
        <td>
            1-Também chamada de <b>BPC</b> (bloco controle de processo)
        </td>
        <td>
            2-Contem informações de contexto de cada processo (ex <b>ponteiros de arquivos abertos</b>, posição do
            proximo byte a ser lido em cada arquivo, etc.)
        </td>
        <tr>
            <td>
                3-Contém <b>informações necessarias para trazer o processo de volta</b>, caso o SO tenha que tira-lo de
                execução.
            </td>

            <td>
                4-Contem estados de um processo em um determinado tempo
            </td>
        </tr>
    </table>
    <table>
        <td>
            1-O BCP <b>só não guarda o conteudo.</b>
        </td>
        <tr>
            <td>
                Assim, um processo é <b>constituido de seu espaço de endereçamento e BCP</b>(com seus registradores,
                etc.) representando uma entrada na tabela de processos
            </td>
        </tr>
    </table>
    <h2 id="c">estados de um processo</h2>
    <ol>
        <li> <strong>execuntando</strong>: realmente usando a CPU naquele momento.</li>
        <li> <strong>bloqueado</strong> : incapaz de executar enquanto um evento externo não ocorrer.</li>
        <li><b>Supenso</b>: o processo ja foi submetido porem ficara suspenso ate que o horario ou evento programado
            aconteça. Exemplo: um backup agendado</li>
        <li><b>Espera</b>: é o processo que esta colocado na fila de espera, e esperandouma interação do usuario.
            Exemplo: autenticação atraves de usuario e senha.</li>
        <li><strong>Pronto</strong>: em memoria, pronto para executar (ou para continuar sua execução), apenas
            aguardando a disponibilidade do processador</li>
        <li><b>Completo</b>: O processo ja foi processado por completo.</li>
    </ol>
    <address>
        conteudo retirado do canal: <cite> UNIVESP</cite> <br>
        <a href="https://youtu.be/Yb0rViAwVQ0">sistemas_operacionais-Processos</a>
    </address>
    <ul>
    <li><a href="#inicio">volte ao inicio</a></li> 
    <li> <a href="processo2.html">prcessos_continuação</a></li>
    </ul>
</body>

</html>
