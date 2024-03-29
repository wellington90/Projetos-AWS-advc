<body lang="pt-BR" link="#000080" vlink="#800000" dir="ltr"><p style="font-variant: normal; letter-spacing: normal; font-style: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 16pt"><b>O Desafio ADVC da CloudFaster Academy envolve a configuração de uma infraestrutura na nuvem usando a Amazon Web Services (AWS). Os participantes criam uma VPC na região N. Virginia com 4 subnets, 2 públicas e 2 privadas, e estabelecem conectividade à internet para as subnets privadas por meio de um NAT Gateway altamente disponível.

Eles também criam Security Groups para o Application Load Balancer (ALB) e as instâncias EC2, permitindo acesso à porta 80 apenas para o ALB. Um Target Group é configurado para conectar o ALB às instâncias EC2.

O próximo passo envolve a criação de um Launch Template e um Auto Scaling Group para gerenciar as instâncias EC2, com configurações de rede, capacidade e escalabilidade definidas. Os participantes testam a resiliência do sistema desligando uma instância e observando o Auto Scaling Group substituí-la automaticamente.

O Desafio ADVC proporciona uma oportunidade valiosa para os profissionais adquirirem experiência prática em configurar e gerenciar infraestrutura na nuvem usando a AWS.</b></font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_e4ca639403cb0399.png" name="Image1" alt="arquitetura-desafio-advc.png" align="bottom" width="1200" height="700" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="var bs-body-font-family"><font size="2" style="font-size: 10pt"><b><span style="background: transparent">Passo
a passo:</span></b></font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; line-height: 100%; orphans: 2; widows: 2; margin-bottom: 0.5cm">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="var bs-body-font-family"><font size="2" style="font-size: 10pt"><span style="background: transparent">O
	Ambiente do Desafio deve ser provisionado na Região N. Virginia
	(us-east-1)</span></font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="var bs-body-font-family"><font size="2" style="font-size: 10pt"><span style="background: transparent">Acesse
	a conta com os dados fornecidos pela CloudFaster Academy</span></font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="var bs-body-font-family"><font size="2" style="font-size: 10pt"><span style="background: transparent">Em
	seguida navegue até o serviço de VPC e vamos criar uma VPC</span></font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_6f1c2a64df5b337e.png" name="Image2" alt="img_001.png" align="bottom" width="698" height="410" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Essa
	VPC deve ter o endereço 10.77.0.0/16 com 4 Subnets, sendo 2
	públicas e 2 privadas.</font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">As
	subnets privadas devem ter comunicação com a internet via NAT
	Gateway</font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">A
	implementação do NAT Gateway deve ser feita com alta
	disponibilidade</font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Pode
	ser utilizado o criado de VPC para provisionar os recursos de forma
	otimizada e automática.</font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_8305d70d97d0d899.png" name="Image3" alt="img_002.png" align="bottom" width="703" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Após
	usar o configurador de VPC, aguarde até que seja provisionado todos
	os recursos, geralmente leva uns 2 minutos até o NAT Gateway ser
	provisionado, aguarde:</font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_b139d28ea0526d.png" name="Image4" alt="img_003.png" align="bottom" width="702" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Perceba
que a criação otimizada, pular várias etapas que poderíamos
realizar manualmente, o bom profissional entende cada uma dessas
etapas.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Não
tem problema utilizar o configurador, mas reserve um tempo para
estudar cada componente da VPC, isso te diferencia no mercado e te
ajudar a ter mais confiança no dia a dia.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_1c7946ead242b62b.png" name="Image5" alt="img_004.png" align="bottom" width="699" height="760" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">VPC
criada com sucesso.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Ao
	clicar em Visualizar VPC, você tem acesso a um Mapa de recursos da
	VPC, que pode te ajudar verificar se você provisionou a VPC
	corretamente, se tiver algum problema, finalize o LAB, aguarde 2
	minutos, abra um novo LAB e refaça a criação da VPC para seguir:</font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_eb64edd5d5e72fc8.png" name="Image6" alt="img_005.png" align="bottom" width="703" height="272" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Ainda
	no serviço de VPC, do lado esquerdo, selecione o componente do
	Security Group (Grupo de Segurança) e crie um Security Group de
	nome SG-DO-ALB (que vai ser usado no ELB)</font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_66c53c31d716cf80.png" name="Image7" alt="img_006.png" align="bottom" width="679" height="634" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Ao
criar o Grupo de Segurança, certifique-se de que esteja criando o
Grupo de Segurança na VPC que você criou, aqui está um ponto que
vários cometem erros,&nbsp;<b>atenção!</b></font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_39d369ba395eba9d.png" name="Image8" alt="img_007.png" align="bottom" width="691" height="587" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Nesse
security group, crie a regra que libere o acesso de entrada a porta
80 para 0.0.0.0/0 (internet)</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_740a5581f57999b8.png" name="Image9" alt="img_008.png" align="bottom" width="681" height="577" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Finalize
a criação do grupo clicando no fim da página em&nbsp;<b>Criar
grupo de Segurança</b>:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_107161377b1ad979.png" name="Image10" alt="img_009.png" align="bottom" width="380" height="103" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Repita
	o processo e crie um Security Group de nome SG-DA-EC2 (que vai ser
	usado na EC2)</font></font></p>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Nesse
	security Group, libere apenas o SG_ELB como origem de quem pode
	acessar sua EC2 na porta HTTP / 80.</font></font></p>
</ul>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_235303df0eb15b2d.png" name="Image11" alt="img_010.png" align="bottom" width="697" height="750" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Essa
configuração visa segurança no acesso a nossa aplicação que vai
rodar na EC2, apenas o ALB vai ter acesso via HTTP porta 80 na EC2.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Selecione
o SG do ALB, e finalize a criação do Security Group.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Se
você seguir os passos corretamente, temos agora 2 Security Group
criados.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">1
para usarmos no ALB</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">1
para usarmos com as EC2</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Vá
até o serviço do EC2</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Do
lado esquerdo no menu, na seção “Balanceamento de carga”,
clique na opção “Grupos de destino”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Aqui
vamos criar o “Grupo de destino”, também chamado de TARGET
GROUP, que faz a comunicação do ALB com as EC2.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Antes
de criar o ALB precisamos criar esse recurso, vamos lá:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_70fb2b50acfa0416.png" name="Image12" alt="img_011.png" align="bottom" width="684" height="601" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clicou
em criar grupo de destino, em seguida escolha o tipo de destino.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Aqui
vamos trabalhar com “Instâncias”, dê um nome para o seu destino
como na imagem de exemplo usamos “destino-ec2-advc”, deixe como
HTTP na porta 80, pois é o protocolo e porta que vamos rodar nossa
aplicação e deixe como IPv4.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_80c940f1d0e74a1d.png" name="Image13" alt="img_012.png" align="bottom" width="693" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Mais
pra baixo, ainda nessa configuração, muita atenção, precisa
selecionar a VPC que criamos para este projeto, em verificação de
integridade deixe como está, e pode clicar em “Próximo” para
criar.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_47e591b8cf6e8a59.png" name="Image14" alt="img_013.png" align="bottom" width="672" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Na
próxima tela é uma opção para “Registrar destinos”, como
ainda não temos as EC2, não temos nada para adicionar aqui, vamos
apenas confirmar clicando no botão “Criar grupo de destino”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_61469d8c724e90a4.png" name="Image15" alt="img_014.png" align="bottom" width="681" height="666" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Pronto,
nosso grupo de destino foi criado:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_85d5f11a47dd48ec.png" name="Image16" alt="img_015.png" align="bottom" width="697" height="860" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Você
verá uma tela semelhante a esta!</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<ul>
	<li><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
	<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Agora
	do lado direito, ainda no menu de EC2, na seção “Balanceamento
	de carga” clique em “Load Balancers” ou “Balanceamento de
	carga” dependendo do navegador pode traduzir, aqui vamos criar um
	Application Load Balancer.</font></font></p>
</ul>
<p align="center" style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_519a0b88f8d148b4.png" name="Image17" alt="img_016.png" align="bottom" width="689" height="638" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Após
clicar em Criar load balancer</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Devemos
selecionar o tipo, vamos usar aqui o Application Load Balancer</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_a07d8a8edd2bcbd9.png" name="Image18" alt="img_017.png" align="bottom" width="691" height="1107" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Tenha
bastante atenção nessa configuração, o índice de erros é alto
nesse tipo de laboratório.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Aqui
é onde você configura o nome do balanceador.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Seleciona
que ele é voltado a internet, ou seja, ele vai receber requisições
da internet.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Defina
o tipo de endereço IP que ele vai trabalhar, vamos no básico IPv4.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">E
principalmente, onde o pessoal erra muito, precisa escolher a VPC que
criamos, e precisa apontar as subnets públicas. Aqui o pessoal erra
bastante.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_4d81ca76c2624b90.png" name="Image19" alt="img_018.png" align="bottom" width="691" height="1214" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Mais
abaixo, temos a configuração do Grupo de Segurança.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Por
isso criamos eles antes, para que vocês selecionem aqui exatamente o
Grupo de Segurança já definido antes.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_6df8f097358a2ace.png" name="Image20" alt="img_019.png" align="bottom" width="701" height="345" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Depois,
em “Listeners e roteamento” vamos deixar HTTP porta 80 e vamos
definir o grupo de destino, ou seja, para onde vamos encaminhar quem
chegar no balanceador, e aqui vamos conectar com o Grupo de Destino,
selecione o que acabamos de criar:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_bb6710cb3d4d106a.png" name="Image21" alt="img_020.png" align="bottom" width="695" height="367" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Pode
descer e embaixo clicar em “Criar load balancer”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_f8ae2e41859e22f3.png" name="Image22" alt="img_021.png" align="bottom" width="314" height="85" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Se
tudo correu bem, vai ser exibido a mensagem de criação em
andamento, se você clicar em listar os Load Balancers, a tela vai
listar o balanceador com Status de “Em provisionamento”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_9193a6a1b3d3224.png" name="Image23" alt="img_022.png" align="bottom" width="683" height="253" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Selecionando
o balanceador e clicando em detalhes, você pode ver o endereço DNS
do balanceador, ainda não tem nada vinculado para responder neste
endereço, mas é ele que vamos usar para testar nossa aplicação
depois que provisionar as EC2 com a nossa aplicação.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Já
salva ele num bloco de notas pois vamos precisar consultar esse
endereço logo mais.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_cb8434182d2810c3.png" name="Image24" alt="img_023.png" align="bottom" width="655" height="346" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Agora
ainda no Menu de EC2, na seção de “Instâncias” vamos criar um
“Modelo de Execução (launch template)</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_4afbee99a630de9f.png" name="Image25" alt="img_024.png" align="bottom" width="697" height="473" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Considerações
para o Modelo de Execução:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Dê
um nome para seu modelo, exemplo: template-advc</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Em
seguida uma descrição ex: teste</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Pode
marcar a opção de fornecer orientações para usar com EC2 Auto
Scaling.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_fbae9f879cfdcb8.png" name="Image26" alt="img_025.png" align="bottom" width="672" height="533" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Selecionar
a AMI Amazon Linux</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Em
tipo de instância nesse desafio vamos usar o tipo t2.micro</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_6768d7f54dfd96ae.png" name="Image27" alt="img_026.png" align="bottom" width="643" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Não
precisa criar par de chave, você não precisa logar na EC2, então
marque sem um par de chaves.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Em
configurações de Rede, selecione a opção “Não incluir no
modelo de execução”, faremos isso depois no Auto Scaling.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Selecione
o grupo de segurança para as EC2 criado anteriormente.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_3608eadb5e1a0eef.png" name="Image28" alt="img_027.png" align="bottom" width="688" height="683" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Nas
configurações de Storage (volume) e Tags de recurso não precisa
alterar nada no momento.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Mas
precisamos de uma configuração específica nos detalhes avançados,
e aqui está outro local de muito erro, preste atenção.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Não
se esqueça de passar as instruções de user data para provisionar a
aplicação nos dados opcionais dos Detalhes avançados.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Aqui
também precisamos marcar a opção que permite a leitura da TAG Name
da EC2: “Permitir etiquetas em metadados” precisa ser HABILITADO
nos detalhes avançados na hora de criar o modelo de execução.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Abaixo
dessa opção, fica a caixa para você colocar o código que será
responsável pela execução da sua aplicação web. “Dados de
usuário” cole o código a seguir:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Note:
Estas 2 ações, são umas das últimas opções da guia de detalhes
avançados, role até encontrá-las:- Criar uma VPC com endereçamento
10.77.0.0/16</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_316ef6dc41346c00.png" name="Image29" alt="img_028.png" align="bottom" width="692" height="508" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Código
para provisionar a aplicação:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2">
<br/>
<br/>

</p>
<pre class="western" style="margin-bottom: 0.25cm; border-top: 1px solid #989898; border-bottom: 1px solid #989898; border-left: 1px solid #989898; border-right: none; padding-top: 0.05cm; padding-bottom: 0.05cm; padding-left: 0.05cm; padding-right: 0cm"><font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">#cloud-config</font></font>
<font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">package_update: true</font></font>
<font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">packages:</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- httpd</font></font>
<font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">runcmd:</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- wget -O /usr/local/init_faster.sh https://assets.cloudfaster.academy/danrezende/scripts/init_faster.sh</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- chmod +x /usr/local/init_faster.sh</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- sh /usr/local/init_faster.sh</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- service httpd start</font></font>
    <font face="var bs-font-monospace"><font size="2" style="font-size: 10pt">- chkconfig httpd on</font></font></pre><p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clique
em “Criar modelo de Execução”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">E
essa tela será exibida:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_83c68e5918d4f6df.png" name="Image30" alt="img_029.png" width="671" height="424" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clique
em visualizar o modelo de execução e está algo como esta tela:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_d32bf44a4b048ffc.png" name="Image31" alt="img_030.png" align="bottom" width="681" height="159" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Em
ainda no menu de EC2, navegue até do lado esquerdo lá em baixo na
seção de Auto Scaling, clique em Grupos Auto Scaling</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_91b2f9530d10a2f1.png" name="Image32" alt="img_031.png" align="bottom" width="678" height="517" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">As
configurações que vamos fazer aqui, vão definir quantas instâncias
EC2 serão provisionada:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clique
em: Criar modelo de execução.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Agora
vamos criar o Grupo de Auto Scaling do Amazon EC2 Auto Scaling</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Na
etapa 1, vamos definir um nome para o seu grupo de autoscaling,
exemplo: asg-advc, depois selecione o modelo de execução criado
anteriormente e avance.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_793fe5ad032fb72c.png" name="Image33" alt="img_032.png" align="bottom" width="682" height="739" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Na
Etapa 2, vamos configurar a rede que será usada para provisionar as
EC2 pelo serviço do Auto Scaling, selecionar a VPC que você criou,
e selecionar as 2 subnets privadas que foram criadas.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Nesse
ponto queremos que as nossas instâncias EC2 sejam provisionadas na
subnet privada, pois quem vai ficar exposto para internet é o ALB
(Balanceador de carga), as instâncias EC2 ficaram na subnet privada
para maior segurança.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_2b649e4d04245fc7.png" name="Image34" alt="img_033.png" align="bottom" width="696" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Na
etapa 3, vamos configurar o balanceador de carga, marque a opção de
Anexar a um balanceador de carga existente, na caixa abaixo, marque o
Grupo de Destino criado anteriormente.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_fca39fc9a1c879ff.png" name="Image35" alt="img_034.png" align="bottom" width="691" height="874" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Desça
até a opção de “Verificações de integridade” e ative as
verificações</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clique
no próximo.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_212481e63d420361.png" name="Image36" alt="img_035.png" align="bottom" width="701" height="768" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Na
etapa 4, defina a capacidade desejada, pode definir como 4.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Em
escalabilidade, deixe o mínimo de 4, e máximo de 8.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_62de8e9f31a9efed.png" name="Image37" alt="img_036.png" align="bottom" width="684" height="739" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Clique
no botão próximo.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Depois
novamente em próximo.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_f845a850a53c6b30.png" name="Image38" alt="img_037.png" align="bottom" width="667" height="706" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_be438931fd3514f8.png" name="Image39" alt="img_038.png" align="bottom" width="671" height="187" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Não
precisa adicionar TAG para esse teste e em seguida revise e clique em
“Criar Grupo de Auto Scaling”</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_d5f4dce0ef511216.png" name="Image40" alt="img_039.png" align="bottom" width="251" height="70" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Se
tudo ocorreu bem, você vai ver o status:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_6177840bec0fa083.png" name="Image41" alt="img_040.png" align="bottom" width="676" height="151" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Se
você for rápido, mudar de serviço, listar as instâncias EC2, você
vai ver as 4 máquinas de uma vez, subindo automagicamente, assim:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_b774c4854d883e40.png" name="Image42" alt="img_041.png" align="bottom" width="683" height="256" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Nesse
momento as instâncias EC2 já serão criadas.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Aguarde
de 2 a 3 minutos até que elas estejam saudáveis.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">O
próprio grupo de execução que criamos, fará o trabalho de
registrar as instâncias EC2 no target group do Balanceador de carga.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Sendo
assim, em alguns instantes você pode testar o endereço de DNS do
Application Load Balancer no navegador que você já deve ter
resposta do serviço web.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Faça
um passo adicional enquanto as instâncias são provisionadas.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Vá
até a lista de instâncias EC2, e nomeie as instâncias, para que
você tenha referência de qual máquina está acessando quando
testar a aplicação.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Exemplo:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_5484db8ae61cbfe2.png" name="Image43" alt="img_042.png" align="bottom" width="679" height="213" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Após
as instâncias estarem devidamente nomeadas e no status de
“Executando”, vamos pegar o endereço de DNS do ALB e testar,
lembre-se aqui pode demorar uns 2, a 5 minutos até a EC2 ligar, o
script que instala a aplicação subir, o serviço na porta 80 ficar
disponível, ser registrado no ALB, pra poder funcionar.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Após
esperar uns 2 minutos:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Vá
até o menu do Load Balancer à esquerda, selecione o load balancer e
copie o endereço de DNS, será algo semelhante a este:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_ec4f468c36b24bf5.png" name="Image44" alt="img_043.png" align="bottom" width="692" height="451" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Copie
o endereço e cole no navegador.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Observe
pois talvez o seu navegador, Google Chrome costuma fazer isso, vai
inserir um HTTPS na URL, e nesse momento a aplicação ainda não
está pronta para HTTPS, precisa usar HTTP para este teste.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Teste
a aplicação no navegador.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Fique
dando F5 no navegador pois hora ou outra ele vai balancear o tráfego
e você vai se conectar em outra instância.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Se
você observar, o ID da instância vai mudando conforme o
balanceamento de carga vai acontecendo, uma página semelhante a esta
será exibida:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_9ea41fba366f4bbf.png" name="Image45" alt="img_044.png" align="bottom" width="647" height="421" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Teste
a resiliência, desligando uma instância e observe se o EC2 Auto
Scaling vai provisionar uma nova instância no lugar após
identificar que a instância foi desligada (simulando uma falha), em
torno de 5 a 7 minutos uma nova instância será criada, fique
observando no painel da EC2.</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Exemplo:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Desliguei
a instância que tinha nome de ADVC-3</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">E
veja que automaticamente após alguns minutos iniciou-se uma nova
instância para repor a instância que foi identificada como não
saudável:</font></font></p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<img src="./image/index_html_9c98f391801e6fb4.png" name="Image46" alt="img_045.png" align="bottom" width="641" height="260" border="0"/>
</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<br/>

</p>
<p style="font-variant: normal; letter-spacing: normal; font-style: normal; font-weight: normal; orphans: 2; widows: 2; margin-bottom: 0cm">
<font face="Roboto, sans-serif"><font size="2" style="font-size: 10pt">Parabéns!
Você finalizou esse laboratório!</font></font></p>
<p style="line-height: 100%; margin-bottom: 0cm"><br/>

</p>
</body>
</html>
