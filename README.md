# loja-servico


Erro 404 corrigido, alterar em applicationContext.xml:

(estava digitado LojaServicoDBDataSource, o certo seria: LojaServicoBDDataSource.)

<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
	xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:context="http://www.springframework.org/schema/context"
	xsi:schemaLocation="http://www.springframework.org/schema/beans 
			http://www.springframework.org/schema/beans/spring-beans-3.2.xsd
			http://www.springframework.org/schema/context
	http://www.springframework.org/schema/context/spring-context-3.2.xsd">
	<bean id="LojaServicoBDDataSource" class="org.springframework.jndi.JndiObjectFactoryBean"> 
		<property name="jndiName">
			<value>java:comp/env/jdbc/LojaServicoBD</value>
		</property>
	</bean> 	
</beans>

------------------------

Problema novo: conseguir adicionar os produtos no carrinho para depois ir para a pagina de autenticaçao.
