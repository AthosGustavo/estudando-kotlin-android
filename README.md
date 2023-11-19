# Estudando kotlin, Android nativo.

## -------- Documento em constante edição --------


Activity
uma activity possui uma view e a logica

view = entidade

### Criando uma Activity como view principal

1-construa uma classe que herdar de Activity()

2-Declare a Activity no arquivo AndroidManifest

3-Abra uma tag activity com o nome da classe que herdar activity

4-Dentro da tag activity abra a tag intent-filter

5-dentro da tag intent-filter abra uma tag action para declara a activity como view principal atraves do ´MAIN´

6-dentro da tag intent-filter abra a tag category para sinalizar que ela será lançada no momento que o aplicativo for aberto atraves do ´LAUNCHER´


### Método onCreate
			
 - Esse método é chamado quando a Activity está sendo criada pela primeira vez ou quando há uma mudança de configuração,como uma rotação do dispositivo.

### Assinatura do método (savedInstanceState: Bundle?)
			
 - Bundle: O argumento savedInstanceState é do tipo Bundle que é um objeto que contém dados que podem ser usados para restaurar o estado da Activity a partir de uma instância anterior.

 - O Bundle vem acompanhado de uma ´?´ pois ele pode ser nulo e isso acontecerá caso o aplicativo estiver sendo iniciado pela primeira vez.


### Views
			
 - As views são componentes que o usuário irá interagir,a exemplo de inputs,texto e botões.Além disso, elas são semelhantes as tags html


EXEMPLO

val meuBotao = Button(context)
<button>Meu Botão</button>

### Context
			
 - Classe que fornece acesso a recursos e serviços específicos da aplicação ou do sistema operacional.

 - A necessidade do context surge porque muitas operações que uma View pode executar dependem de recursos e configurações específicas da aplicação ou do sistema. Passar o context como parâmetro permite que a View acesse essas informações relevantes.

EXEMPLO

val meuTexto = TextView(context)

 - A TextView pode usar o context para acessar o tema da aplicação, os recursos de string, dimensões, estilos e outras configurações específicas do contexto.


### Layout
					
 - Refere-se à estrutura que define a organização e a aparência visual dos elementos da interface do usuári em uma tela.

 - Layouts são utilizados para organizar Views
 - Os layouts em Android são geralmente definidos em arquivos XML no diretório res/layout/ do projeto. Cada arquivo XML de layout descreve a hierarquia de Views e suas propriedades.

### Método setContentView

Método usado para renderizar o layout da interface do usuário associada a essa Activity.O método especifica qual layout XML deve ser usado.


### Classe R

 - Classe R possui a capacidade de acessar arquivos que estão dentro da pasta res.
 - EXEMPLO DE ACESSO: setContentView(R.layout.nomeArquivoXML)

 - uma tag textView nao pode ser aberta dentro de outra tag textView

### Views aninhadas
			
No desenvolvimento android, um botao não pode ser colocado dentro de outro botao e nem dentro de um texto, sendo assim temos as viewsGroup para resolver esses problemas

As viewsGroup usam constraints(restrições) para definir as posições e tamanhos dos elementos filhos em relação uns aos outros e permite possuir outra viewGroup como filha.

				      
### ViewGroups
				      
ConstraintLayout
 - Permite posicionar Views de maineira mais livre e complexa.
 - util para criar layouts responsivos

LinearLayouts
 - Esse tipo de layout é usado para organizar as views de maneira mais fácil e simples.O Linear e apnas permite organizar todas as views na direção horizontal ou vertical.
