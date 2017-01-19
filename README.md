# UAUEmpObra
Controle para selecionar empresa/obra

##Instalação
---------
Inclua os arquivos abaixo na sua página

```html
    <!--angularjs scripts/modules -->
    <script src="<%=ResolveUrl("~/")%>Scripts/angularjs/angular.min.js"></script>
    
    <!-- ui-select files -->
    <script src="<%=ResolveUrl("~/")%>UAUComponente/lib/select/js/select.js"></script>

    <!-- themes -->
    <link href="<%=ResolveUrl("~/")%>UAUComponente/lib/select/css/select2.css" rel="stylesheet" />
    <link href="<%=ResolveUrl("~/")%>UAUComponente/lib/select/css/selectize.default.css" rel="stylesheet" />
    <link href="<%=ResolveUrl("~/")%>UAUComponente/lib/select/css/select.css" rel="stylesheet" />
    <link href="<%=ResolveUrl("~/")%>UAUComponente/src/uau-componente.css" rel="stylesheet" />
    <link href="<%=ResolveUrl("~/")%>UAUComponente/lib/grid/css/ui-grid.min.css" rel="stylesheet" />
 
    <!--scripts uau -->    
    <script src="<%=ResolveUrl("~/")%>UAUComponente/src/uau-common.js"></script>
    <script src="<%=ResolveUrl("~/")%>UAUComponente/src/uau-componente.js"></script>
    
    <!-- EmpObra -->
    <script src="<%=ResolveUrl("~/")%>UAUComponente/diretivas/SelEmpObra/SelEmpObraDirective.js"></script>
```

Adicione na pagina o elemento abaixo, que corresponde ao controle de seleção de Empresa/Obra
```html
<!--DIRETIVA SELECIONAR EMPRESA/OBRA-->
<div ng-controller="ctrlEmpobra as ctrl">
    <uau-empobra obrasel="obrasel" modoselecao="simples"></uau-empobra>
</div>
```

Para obter a Empresa/Obra selecionada, basta adicionar o código abaixo em qual quer controller.
```javascript
//Recebe o evento ao selecionar empresa e obra
$rootScope.$on('EMPRESAOBRAEVENT', function (e, data) {
    //Chamada do serviço para salvar empresa e obra
    alert(data);
});
```
