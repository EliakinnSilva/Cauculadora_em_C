# Cauculadora_em_C

#Apresentação do codigo

stdio.h: fornece funções para entrada e saída de dados.
string.h: contém funções para manipulação de strings.
stdlib.h: contém a função strtok para dividir uma string em tokens.
Definição da constante TAM_MAX com o valor 30.

#Definição da estrutura contato que contém campos para o nome e telefone.

#Declaração das funções utilizadas no programa: cadastrarContato, buscarContato, editarContato, excluirContato, exportarAgenda e importarAgenda.

#Função cadastrarContato:

Recebe como parâmetros um array de contatos agenda, o ponteiro para o número de contatos numContatos e o ponteiro para um arquivo.
Verifica se o número de contatos é menor que TAM_MAX (30) para evitar que a agenda fique cheia.
Solicita ao usuário que digite o nome e telefone do novo contato.
Adiciona o novo contato à agenda e incrementa o número de contatos.
Imprime uma mensagem informando que o contato foi cadastrado com sucesso.

#Função buscarContato:
Recebe como parâmetros um array de contatos agenda, o número de contatos numContatos, o nome do contato a ser buscado nomeBusca e um valor booleano imprimirInfo para determinar se as informações adicionais do contato serão impressas.
Realiza uma busca binária na agenda para encontrar o contato com o nome especificado.
Se o contato for encontrado, imprime suas informações.
Se imprimirInfo for verdadeiro, imprime informações adicionais sobre o contato.

#Função editarContato:
Recebe como parâmetros um array de contatos agenda, o número de contatos numContatos e o nome do contato a ser editado nomeBusca.
Percorre a agenda em busca do contato com o nome especificado.
Se o contato for encontrado, imprime suas informações, solicita ao usuário que digite as novas informações e as atualiza.
Imprime uma mensagem informando que o contato foi editado com sucesso.

#Função excluirContato:
Recebe como parâmetros um array de contatos agenda, o ponteiro para o número de contatos numContatos e o nome do contato a ser excluído nomeBusca.
Percorre a agenda em busca do contato com o nome especificado.
Se o contato for encontrado, realiza o deslocamento dos contatos para preencher o espaço vazio e decrementa o número de contatos.
Imprime uma mensagem informando que o contato foi excluído com sucesso.

#Função exportarAgenda:
Recebe como parâmetros um array de contatos agenda, o número de contatos numContatos e o nome do arquivo nomeArquivo.
Abre o arquivo no modo de escrita.
Percorre a agenda e escreve as informações de cada contato no arquivo.
Fecha o arquivo.
Imprime uma mensagem informando que a agenda foi exportada com sucesso.

#Função importarAgenda:
Recebe como parâmetros um array de contatos agenda, o ponteiro para o número de contatos numContatos e o nome do arquivo nomeArquivo.
Abre o arquivo no modo de leitura.
Lê cada linha do arquivo e divide a linha em nome e telefone utilizando a função strtok.(A função strtok é comumente usada para dividir uma string em palavras separadas por espaços em branco ou outros caracteres delimitadores. )
Copia o nome e telefone para um novo contato na agenda e incrementa o número de contatos.
Fecha o arquivo.
Imprime uma mensagem informando que a agenda foi importada com sucesso.

#Função main:
Declaração das variáveis locais: agenda (array de contatos), numContatos (número de contatos), opcao (opção selecionada pelo usuário) e nomeBusca (nome do contato a ser buscado ou editado).
Inicia um loop infinito para exibir o menu e aguardar a escolha do usuário.
Dentro do loop, exibe o menu de opções e solicita ao usuário que escolha uma opção.
Utiliza um switch-case para executar a função correspondente à opção selecionada.
Se a opção for 0, encerra o loop e o programa.
Ao final do programa, retorna 0 para indicar que a execução foi concluída com sucesso.
