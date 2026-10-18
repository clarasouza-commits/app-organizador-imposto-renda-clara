Organizador de Imposto de Renda (LION APP)

Ferramenta em Excel que reúne e organiza as informações essenciais para a declaração de Imposto de Renda da pessoa física. Foi construída para ter cara de aplicativo: menu de navegação lateral, botões, formas, hiperlinks, listas suspensas e validações automáticas, tudo dentro do próprio Excel, sem macros.

Projeto prático do desafio da DIO.

Todos os dados da planilha (nome, CPF, bancos, valores) são fictícios, só de exemplo.

Prints
Aba TITULAR	Aba INFORMES	Aba NOTAS
Mostrar Imagem	Mostrar Imagem	Mostrar Imagem
O que a ferramenta faz

A planilha tem três abas visíveis e uma aba oculta de apoio.

Aba	Para que serve
TITULAR	Dados da pessoa física: nome, CPF, nascimento, título de eleitor, cônjuge, endereço, CEP, telefones, e-mail e três perguntas de SIM/NÃO (houve alterações da entrega anterior, dependente cônjuge, residente do exterior).
INFORMES	Informes de rendimentos bancários de até 3 bancos: banco, valor atual e nome do arquivo anexo. Mostra o total somado.
NOTAS	Entradas de receita mês a mês (data, categoria e valor), numa tabela do Excel. Mostra o total de entradas.
TABELAS (oculta)	Lista de 50 bancos usada na lista suspensa da aba INFORMES.
Botões, formas e hiperlinks
Menu lateral em todas as abas, com o título LION APP, o logo e três botões arredondados (TITULAR, INFORMES, NOTAS). Cada botão tem um hiperlink para a aba correspondente, e o botão da aba atual aparece destacado.
Botões PRÓXIMO e ANTERIOR no fim de cada aba (e no topo da aba NOTAS), para navegar em sequência.
Links rápidos na barra lateral, que abrem no navegador o site da Receita Federal e o serviço "Meu Imposto de Renda".
Todos os botões têm uma dica que aparece ao passar o mouse.

Os botões são formas do Excel (retângulos e retângulos de cantos arredondados) com hiperlink, inseridas pelo menu Inserir > Formas.

Validações automáticas
Onde	Regra
TITULAR, D17:D19	Lista suspensa com SIM ou NÃO.
TITULAR, CPF	Aceita só um número de até 11 dígitos.
TITULAR, nascimento	Exige uma data válida que não seja futura.
TITULAR, CEP, telefone e celular	Aceitam só números, com a quantidade certa de dígitos.
TITULAR, e-mail	Exige um endereço com @.
INFORMES, banco	Lista suspensa com os 50 bancos da aba TABELAS, usando o intervalo nomeado lista_bancos.
INFORMES, valor atual	Aceita só valores maiores ou iguais a zero.
NOTAS, categoria	Lista suspensa com HOLERITE, CNPJ ou FREELANCE.
NOTAS, data e valor	Aceitam só data válida e valor maior ou igual a zero.

Quando o usuário digita algo fora da regra, o Excel mostra uma mensagem de erro explicando o que corrigir.

Formatação e cálculos
As células amarelas são de preenchimento do usuário. As células verdes são calculadas (os totais) e não devem ser editadas.
Total em INFORMES (C7): soma os valores dos três bancos, =SOMA(D11;D16;D21).
Total em NOTAS (E5): soma a coluna de valores, =SOMA(E9:E35).
CPF, CEP e telefones aparecem com máscara (por exemplo, 123.456.789-09), mas são guardados como número.
As linhas de grade e os títulos de linhas e colunas estão ocultos, para a planilha parecer um aplicativo.
Intervalo nomeado
Nome	Referência	Uso
lista_bancos	TABELAS!A2:A51	Lista suspensa de bancos em INFORMES
O que mudei em relação ao modelo
Visual próprio: troquei o rosa e roxo do modelo por verde, dourado e creme, combinando com o logo do leão.
Logo próprio na barra lateral, com fundo transparente.
Título corrigido: o modelo escreve "TÍTULAR"; no meu está "TITULAR".
Links rápidos para a Receita Federal e o Meu Imposto de Renda na barra lateral.
Mais validações: CPF, CEP, telefone, e-mail, data de nascimento e valores não negativos.
Total de entradas na aba NOTAS, que o modelo não tem.
Datas no formato brasileiro (dd/mm/aaaa) e crédito do sistema com o meu nome.
Dados de exemplo próprios, todos fictícios.
Como usar
Baixe o arquivo Organizador_IR.xlsx neste repositório.
Abra no Excel e use o menu lateral para navegar entre as abas.
Preencha as células amarelas. Os totais são atualizados sozinhos.
Arquivos
Organizador_IR.xlsx: a planilha.
print-titular.png, print-informes.png e print-notas.png: prints de cada aba.
