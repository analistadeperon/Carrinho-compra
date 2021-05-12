# Carrinho-compra
<div id="app"></div>

>

<script>
 function AddCarrinho(produto, qtd, valor, posicao)
 { 
 localStorage.setItem("produto" + posicao, produto);
 localStorage.setItem("qtd" + posicao, qtd);
 valor = valor * qtd;
 localStorage.setItem("valor" + posicao, valor);
 alert("Produto adicionado ao carrinho!");
 }
</script>
<button type="button" id="adicionar1" id="produto1" onclick="AddCarrinho('Sabão', document.getElementById('qtd1').value, '2.00', 1)"> Comprar </button>
localStorage.getItem("nome_do_campo");
<meta charset="UTF-8">
<div id="itens"> </div>
<div>Total: <span id="total"></span> </div>

<script>
 var total = 0; // variável que retorna o total dos produtos que estão na LocalStorage.
 var i = 0;     // variável que irá percorrer as posições
 var valor = 0; // variável que irá receber o preço do produto convertido em Float.
 
 for(i=1; i<=99; i++) // verifica até 99 produtos registrados na localStorage
 {
	 var prod = localStorage.getItem("produto" + i + ""); // verifica se há recheio nesta posição. 
	 if(prod != null) 
	 {	
		 // exibe os dados da lista dentro da div itens
		 document.getElementById("itens").innerHTML += localStorage.getItem("qtd" + i) + " x ";
		 document.getElementById("itens").innerHTML += localStorage.getItem("produto" + i);
		 document.getElementById("itens").innerHTML += " ";
		 document.getElementById("itens").innerHTML += "R$: " + localStorage.getItem("valor" + i) + "<hr>";
		 
		 // calcula o total dos recheios
		 valor = parseFloat(localStorage.getItem("valor" + i)); // valor convertido com o parseFloat()
		 total = (total + valor); // arredonda para 2 casas decimais com o .toFixed(2)
	 }
 } 
 // exibe o total dos recheios
 document.getElementById("total").innerHTML = total.toFixed(2); 
</script>

<button type="button" onclick=" localStorage.clear(); location.reload();"> Limpar carrinho </button>
           <html lang="en">
 
<head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
 
    <title>Bootstrap Shop Cart</title>
 
    <!-- Bootstrap core CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.2/jquery.min.js"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
 
    <style>
        body {
            padding-top: 50px;
        }
        #divTotal{
            background-color: green;
        }
        .affix{
            right: 0px;
        }
        .affix-top{
            right: 0px;
            position: fixed;
        }
    </style>
 
</head>
 
<body>
 
    <div class="container">
 
 
    </div>
 
<div class="row">
   
</div>
<div class="col-xs-7 col-md-8 col-sm-8 col-lg-8">
 
</div>
 
<div class="col-xs-5 col-md-4 col-sm-4 col-lg-4">
     
</div>
<div class="panel panel-primary">
    <div class="panel-heading">
        <h3 class="panel-title">Panel title</h3>
    </div>
    <div class="panel-body">
        <div class="radio">
            <label>
                <input type="radio" name="optradio">Option 1</label>
        </div>
        <div class="radio">
            <label>
                <input type="radio" name="optradio">Option 1</label>
        </div>
        <div class="radio">
            <label>
                <input type="radio" name="optradio">Option 1</label>
        </div>
    </div>
</div>
<div class="panel panel-primary">
    <div id="divTotal" class="panel-heading">
        <h3 class="panel-title">Total</h3>
    </div>
    <div class="panel-body">
        <h2>Rs. 100</h2>
    </div>
</div>
 
<div class="text-center">
    <a href="#/checkout" class="btn btn-danger">Checkout <span class="glyphicon glyphicon-shopping-cart" aria-hidden="true"></span>
    </a>
</div>
<div class="container">
    <div class="well">
        <div class="page-header">
            <h3>Quotation</h3>
        </div>
 
        <table class="table">
            <tr>
                <td>
                    CPU
                </td>
                <td>
                    Rs. 20000
                </td>
            </tr>
            <tr>
                <td>
                    Hard Disk
                </td>
                <td>
                    Rs. 5000
                </td>
            </tr>
            <tr>
                <td>
                    <b>Total:</b>
                </td>
                <td>
                    <b>Rs. 25000</b>
                </td>
            </tr>
        </table>
 
 
    </div>
    <div class="text-left">
        <a type="button" class="btn btn-danger" href="#/cart">Customize <span class="glyphicon glyphicon-pencil" aria-hidden="true"></span></a>
 
    </div>
</div>
use strict';
 
angular.module('checkout', ['ngRoute'])
 
.config(['$routeProvider', function($routeProvider) {
    $routeProvider.when('/checkout', {
        templateUrl: 'public/checkout/checkout.html',
        controller: 'CheckoutCtrl'
    });
}])
 
.controller('CheckoutCtrl', ['$scope', function($scope) {
    
}]);
<script src="public/checkout/checkout.js"></script>
angular.module('shoppingCart', [
    'ngRoute',
    'cart',
    'checkout'
]).

<div class="container-fluid">
    <div class="row">
        <div class="col-sm-9 col-sm-offset-3">
            <button type="button" class="btn btn-primary" id="finalizar">Finalizar Compra</button>
            <button type="button" class="btn btn-danger" id="limpar">Limpar Carrinho</button>
            <button type="button" class="btn btn-success" id="total">Total</button>
        </div>
    </div>
    <div class="row">
        <div class="col-sm-6">
            <fieldset>
               <fieldset class="fsResDir">
  
</fieldset>
<form id="payment-form" target="_blank" action="https://<-- seu servico -->" method="POST">
    <div class="usable-creditcard-form">
      <div class="wrapper">
        <div class="input-group nmb_a">
          <div class="icon ccic-brand"></div>
            <input autocomplete="off" class="credit_card_number" data-iugu="number" placeholder="Número do Cartão" type="text" value="" />
          </div>
        <div class="input-group nmb_b">
          <div class="icon ccic-cvv"></div>
            <input autocomplete="off" class="credit_card_cvv" data-iugu="verification_value" placeholder="CVV" type="text" value="" />
        </div>
        <div class="input-group nmb_c">
          <div class="icon ccic-name"></div>
            <input class="credit_card_name" data-iugu="full_name" placeholder="Titular do Cartão" type="text" value="" />
        </div>
        <div class="input-group nmb_d">
          <div class="icon ccic-exp"></div>
            <input autocomplete="off" class="credit_card_expiration" data-iugu="expiration" placeholder="MM/AA" type="text" value="" />
        </div>
      </div>
      <div class="footer">
        <img src="https://s3-sa-east-1.amazonaws.com/storage.pupui.com.br/9CA0F40E971643D1B7C8DE46BBC18396/assets/cc-icons.e8f4c6b4db3cc0869fa93ad535acbfe7.png" alt="Visa, Master, Diners. Amex" border="0" />
        <a class="iugu-btn" href="http://iugu.com" tabindex="-1"><img src="https://s3-sa-east-1.amazonaws.com/storage.pupui.com.br/9CA0F40E971643D1B7C8DE46BBC18396/assets/payments-by-iugu.1df7caaf6958f1b5774579fa807b5e7f.png" alt="Pagamentos por Iugu" border="0" /></a>
      </div>
    </div>

    <div class="token-area">
        <label for="token">Token do Cartão de Crédito - Enviar para seu Servidor</label>
        <input type="text" name="token" id="token" value="" readonly="true" size="64" style="text-align:center" />
    </div>
       
    <div>
        <button type="submit">Salvar</button>
    </div>
            
  </form>
     
