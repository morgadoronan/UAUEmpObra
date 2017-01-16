# UAUEmpObra
Controle para selecionar empresa/obra

##Instalação
---------
Inclua os arquivos abaixo na sua página

```html
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
