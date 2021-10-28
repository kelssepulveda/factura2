# factura2
factura dos con php y css
<?php

//------uwu---//

$nombre_de_empresa = $_POST["empresa"];
$fecha=$_POST["fecha"];
$logo_de_empresa=$_POST["logo"];
$numero_de_orden=$_POST["orden"];
$direccion=$_POST["direccion"];
$telefono=$_POST["telefono"];
$email=$_POST["mail"];
$sitio_web=$_POST["sitioweb"];

///----VENDEDOR--PARTE IZQUIERDA--///
//---tabla2--//
$nombre_empresa_vendedor=$_POST["empresa_vendedor"];
$contacto_vendedor=$_POST["contacto_vendedor"];
$direccion_de_vendedor=$_POST["direccion_de_vendedor"];
$telefono_vendedor=$_POST["telefono_vendedor"];
$email_vendedor=$_POST["mail_vendedor"];

//----ENVIO A---PARTE DERECHA--//

$nombre_de_empresa_envio = $_POST["empresa_envio"];
$nombre_de_envio= $_POST["nombre_de_envio"];
$direccion_envio = $_POST["direccion_envio"];
$telefono_envio = $_POST["telefono_envio"];
$email_envio = $_POST["mail_envio"];

///---tabla3---///
///---textara1--///

$textarea1=$_POST["texto1"];
$textarea2=$_POST["texto2"];
$textarea3=$_POST["texto3"];

///---tabla4---///

$articulo=$_POST["articulo"];
$descripcion=$_POST["descripcion"];
$cantidad=$_POST["cantidad"];
$p_u=$_POST["precio"];

///---textarea2--/

$textarea4=$_POST["condiciones"];
//--fin--//
$total=array();
$totalfinal=0;
?>
<!DOCTYPE html>
<html>
    <head>

        <title>Formulario</title>

        <meta charset="UTF-8">

        <style>

           .contenedor{
               position: relative;
               width: 65%;
               height: 70%;
               padding-left: 20px;
               padding-top: 10px;
               background-color: hsl(175, 77%, 66%);
               margin: auto;
            }

                table{
                    border: 2px solid #000000;
                    margin-bottom: 10px;
                    border-collapse: collapse;
                    color: #000000;
                    background-color: #75ffa3;
                    width: 95%;
                }

                th{
                    background-color: hsl(352, 83%, 72%);
                    font-family: Georgia, Times, 'Times New Roman', serif;
                    height:10px;
                }


           textarea{
               resize: none;
           }

           input[type=submit]{
               position: relative;
               width: 150px;
               height: 40px;
               margin-left: 430px;
           }
        </style>

    </head>

    <body>

        <div class="contenedor">

            
            <table>
                
        <tr>

            <th colspan="4" align="right">ORDEN DE COMPRA</th>
    
            </tr>
    
            <tr>

                    <td> Nombre de Empresa  :</td><td><?php echo $nombre_de_empresa; ?></td>
                    <td> FECHA : </td><td><?php echo $fecha; ?></td>
            
                </tr>
                
        <tr>

            <td>Logo De Empresa : </td><td><?php echo $logo_de_empresa; ?></td>
            <td>Número de Orden :</td><td><?php echo $numero_de_orden; ?></td>
        
        </tr>

        <tr>

        <td> Dirección : </td><td colspan="3"><?php echo $direccion; ?></td>
    
        </tr>

        <tr>

        <td> Teléfono : </td><td colspan="3"><?php echo $telefono ?></td>
    
        </tr>

    <tr>

        <td> E-mail : </td><td colspan="3"><?php echo $email; ?></td>
    
    </tr>

    <tr>

        <td> Sitio Web : </td><td colspan="3"><?php echo $sitio_web; ?></td>
    
    </tr>

    </table>
    
    <table  class="tabla_2">

        <tr>

            <th colspan="2" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> VENDEDOR </th>
            <th colspan="2" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> ENVIAR A </th> 
       
        </tr>  

        <tr>
            
            <td style="border-bottom:2px solid rgba(0,0,0);"> Nombre De Empresa : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $nombre_empresa_vendedor; ?></td>
            <td  style="border-bottom:2px solid rgba(0,0,0);" > Nombre  : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $nombre_de_envio; ?></td>
        
        </tr>

        <tr>

            <td style="border-bottom:2px solid rgba(0,0,0);"> Contacto o Departamento : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $contacto_vendedor; ?></td>
            <td style="border-bottom:2px solid rgba(0,0,0);"> Nombre De Empresa : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $nombre_de_empresa_envio; ?></td>
        
        </tr>

        <tr>

            <td style="border-bottom:2px solid rgba(0,0,0);"> Dirección : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $direccion_de_vendedor; ?></td>
            <td style="border-bottom:2px solid rgba(0,0,0);"> Dirección : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $direccion_envio; ?></td>
        
        </tr>

        <tr>
            
            <td style="border-bottom:2px solid rgba(0,0,0);"> Teléfono : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $telefono_vendedor; ?></td>
            <td style="border-bottom:2px solid rgba(0,0,0);"> Teléfono : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $telefono_envio; ?></td>
        
        </tr>

        <tr>

            <td style="border-bottom:2px solid rgba(0,0,0);"> E-mail : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $email_vendedor; ?></td>
            <td style="border-bottom:2px solid rgba(0,0,0);"> E-mail : </td><td  style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $email_envio; ?></td>
        
        </tr>

    </table>
    
    <table class="tabla_3">

        <tr>

        <th style="border-right:2px solid rgba(0,0,0);"> Enviado Mediante </th>
        <th style="border-right:2px solid rgba(0,0,0);"> F.O.B</th>
        <th style="border-right:2px solid rgba(0,0,0);"> Condiciones de Envío </th>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0);"><?php echo $textarea1; ?></td>
        <td style="border-right:2px solid rgba(0,0,0);"><?php echo $textarea2; ?></td>
        <td style="border-right:2px solid rgba(0,0,0);"><?php echo $textarea3; ?></td>
    
    </tr>

    </table>

    <table class="tabla_4">

        <tr>

            <th style="border-right:2px solid rgba(0,0,0);"> ARTICULO # </th>
            <th style="border-right:2px solid rgba(0,0,0);"> DESCRIPCIÓN</th>
            <th style="border-right:2px solid rgba(0,0,0);"> CANTIDAD </th>
            <th style="border-right:2px solid rgba(0,0,0);"> P/U </th>
            <th style="border-right:2px solid rgba(0,0,0);"> TOTAL </th>
        
        </tr>

        <tr>



<?php

for ($i=0; $i < 10 ; $i++) { 
    if (empty($cantidad[$i]) or  empty($p_u[$i])) {
    
        ?>

        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> &nbsp </td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> &nbsp </td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> &nbsp </td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> &nbsp </td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> &nbsp </td> 

        </tr>

        <?php

        
    }else{

        $total[$i]=$cantidad[$i]*$p_u[$i];
        $totalfinal=$totalfinal+$total[$i];

        ?>

        <tr>

            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $articulo[$i]; ?></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $descripcion[$i]; ?></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $cantidad[$i]; ?></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $p_u[$i]; ?></td>
            <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $total[$i]; ?></td> 

        </tr>

        <?php
    }
}

?>


















        
        </tr>
   
        <tr>
        
        <th colspan="3" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Condiciones o Instrucciones Especiales </th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Subtotal </th>
        <th style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $totalfinal; ?></th>
    
    </tr>

    <tr>

     <td colspan="3" rowspan="4" style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $textarea4 ?></td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> % Iva </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $iva=$totalfinal * 0.19 ?></td>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Envio</td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> Otro </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"></td>
    
    </tr>

    <tr>

        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"> TOTAL </td>
        <td style="border-right:2px solid rgba(0,0,0); border-bottom:2px solid rgba(0,0,0);"><?php echo $totalfinal + $iva ; ?></td>
    
    </tr> 

    </table>


                      
                      <p> Si tiene alguna duda sobre esta orden de compra , por favor ,pónganse en contacto con :katalinasepulvedalopez@gmail.com</p>
            
    
    </div>

    </body>

</html>
