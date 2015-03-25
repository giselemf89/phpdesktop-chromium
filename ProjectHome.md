# PHP Desktop (Chromium) #

PHP Desktop (Chromium) é um projeto de código aberto desenvolvido por Guilherme Alencar para prover um meio de desenvolver aplicações desktop nativas utilizando tecnologias web como PHP, HTML5, JS e SQLite. Engloba um navegador web (Chromium, uma versão livre do navegador Chrome do Google), um servidor web embutido (nativo da linguagem PHP desde a sua versão 5.4.0), e o interpretador PHP, com a extensão sqlite3 para banco de dados da aplicação.

A idéia é inspirada no conceito de SSB (Site-Specific Browser), que consiste em adaptar um navegador para rodar aplicações web no modo desktop de modo específico para sua aplicação. Em alguns navegadores esta funcionalidade é adicionada com Extensões, mas no Chromium esta função é nativa com a opção -app="site".

Há um outro projeto PHP Desktop, desenvolvido por Czarek Tomczak (http://code.google.com/p/phpdesktop/), no qual este foi inspirado. O meio utilizado por Czarek para alcançar os seus objetivos é distinto, a saber, compilar uma aplicação com a mesma engine do Chrome utilizando um framework chamado CEF (Chromium Embedded Framework), que se assemelhará a um navegador executando o servidor Web PHP embutido num mesmo executável. Isto será muito mais limpo, rápido e menor. O projeto PHP Desktop de Czarek também é mais abrangente, pois pretende alcançar mais navegadores, enquanto este se prende ao Chromium (embora possa ser implementado para outros navegadores também, por meio de extensões, como já referido).

O projeto de Czarek já criou uma aplicação SSB para Microsoft Internet Explorer, o que é vantajoso, pois o projeto é pequeno por rodar a versão do Internet Explorer do Host, e não um Internet Explorer embutido (isto tem vantagens e desvantagens, pois você nunca saberá que versão do Internet Explorer o Host terá instalado).

A versão para Chromium de Czarek ainda não possui release, e este projeto pode ser utilizado enquanto isso não ocorre.

Outras vantagens de se utilizar este projeto é a possibilidade de utilizar recursos do navegador na sua aplicação, como a opção Ctrl+Print (o que não foi implementado ainda no CEF). Também existe a possibilidade de utilização de Extensões do navegador Chromium na sua aplicação, o que pode acrescentar funcionalidades interessantes.

O modo de desenvolver é o mesmo para uma aplicação Web para WAMP (Windows, Apache, MySQL e PHP). Coloca-se a aplicação na pasta www, em que o primeiro arquivo a ser executado deve-se chamar index.php ou index.html. Depois, basta executar o Launcher.exe que executará o servidor PHP (phpdesktop.exe, que é o mesmo executável do php.exe do zip obtido em php.net), e o navegador Chromium apontando para o endereço 127.0.0.1 na porta 54007 (http://127.0.0.1:54007/). Se a janela for fechada, o executável phpdesktop.exe é eliminado da lista de processos do Windows utilizando Javascript e PHP.

Por enquanto o projeto roda apenas em Windows.

## Descrição das Aplicações ##

PHP 5.4.12, Chromium (Portable) 26.0.1410.5, jQuery Javascript Library 1.6.2.

## Extensões do PHP ##

As extensões utilizadas são: cURL, SQLite3, OpenSSL, PDO (SQLite). Outras extensões podem ser utilizadas baixando-se o zip da versão 5.4.12 do php em php.net e colocando a dll desejada em ext/, e depois ativando-a em php.ini. Extensões sugeridas são GD2 (para geração de imagens) e extensões para habilitar suporte a outros bancos de dados (MySQL, PostgreSQL).