ejercicios
==========

mi_repositorio

<?php


echo ejercicio_1(8,9);

    function ejercicio_1($x,$y){
        $a = array(7,6,8,4,9,2,10,0,11,-2);
        if($x<=0 || $x>255 || $y<=0 || $y>255 ){
         return -1;   
        }else{
            
            return $a[$x-1]+$a[$y-1];
        }    
    }
    ?>

<?php
echo ejercicio_2(3,4); 
    
    function ejercicio_2($x, $y){
        
        $semilla=$x;
        if($x<=0 || $x>255 || $y<=0 || $y>255 ){
             return -1; 
        }else{
        
        for($i=2; $i<=$y; $i++){
           $semilla*=$i;
           }
       }
       return $semilla;
            
    }    
    ?>
    
<?php
echo ejercicio_3(60,8); 
    
    function ejercicio_3($x, $y){
        
        $semilla=$x;
        if($x<=0 || $x>255 || $y<=0 || $y>255 ){
             return -1; 
        }else{
        
        for($i=2; $i<=$y; $i++){
           $semilla=$x/$i;
           }
       }
       return $semilla;
            
    }   */
?>

<?php
echo "la cadena 1 se diferencia de la segunda por \"".ejercicio_4("La vida es bella","El santo")."\""; 
    
    function ejercicio_4($x, $y){
        
        for($i=0; $i<strlen($y); $i++){
            $c=substr($y,$i,1);
            $total="";
            for($j=0; $j<strlen($x); $j++){
                 $f=substr($x,$j,1);
                if(strtoupper($c)!=strtoupper($f)){
                   $total.=$f;
                }
            }
            
         $x=$total;
         
        }
    return $total;
    }    
?>

<?php
$x=array(-3,-2,0,0,5,7,9,11,11,25);
print_r(ejercicio_5($x)); 
    
    function ejercicio_5($i){
        return array_values(array_unique($i));;
    } 
?>

<?php
ejercicio_6("hola soy carlos, y todo bien");

function ejercicio_6($str){
    $a=explode(" ",$str);
    for($i=count($a)-1;$i>=0;$i--){
        echo " ".$a[$i];
    }
}
?>

<?php
echo ejercicio_7("Cadena , !/+FFFca 122434");
 
 function ejercicio_7($str){
    $a=array("A","B","C","D","E","F","G","H","I","J","K","L","M","N","Ñ","O","P","Q","R","S","T","U","V","W","X","Y","Z");
    $total="";
    $f=true;
    for($i=0;$i<strlen($str);$i++){
        $c=substr($str,$i,1);
        for($j=0;$j<count($a);$j++){
            if($c==$a[$j]){
                $total.=chr(ord($c)+32);
                $f=false;
                break;
            }else{
                $f=true;
            }
        }
        if($f){
            $total.=$c;
        }
    }
    return $total;
 }
 ?>
 
 <?php
 echo ejercicio_8(". Ah, este es un texto de muestra, que da una lid de análisis" );
 
 function ejercicio_8($str){
    $total=0;
    $siHayA=false;
    for($i=0;$i<strlen($str);$i++){
        $c=substr($str,$i,1);
        if($c=="a" || $c=="A"){
            $siHayA=true;
        }
        if($c==" " || $i==strlen($str)-1){
            if($siHayA){
               $total+=1; 
            }
            $siHayA=false;
        }
    }
    return $total;
 }
 ?>
 
 <?php
 if(ejercicio_9(16)){
    echo "es correcto";
}else{
    echo "es falso";
}

function ejercicio_9($num){
    for($i=1;($i*$i)<$num;$i++){  
    }
    if(($i*$i)==$num){
            return true;            
    }else{
        return false;
    } 
}
?>

<?php
echo ejercicio_10(1,7);
 function ejercicio_10($x,$y){
    for($i=$x;$i<=$y;$i++){
        if(EsNumeroPerfecto($i)){
            return $i;
        }
    }
    return -1;
}
function EsNumeroPerfecto($num){
    $total=0;
    for($j=1;$j<$num;$j++){
      if($num%$j==0){
        $total+=$j;
      } 
    }
    if($total==$num){
        return true;
    }else{
        return false;
    }
}
?>

<?php
$mat=array(1,5,3,-2,4,2,4,-2,5,5,2,1,3);
echo ejercicio_11($mat);

function ejercicio_11($array){
    $cont=0;
    $repetidos = 0;
    $valor=0;
    $ya_duplicados = array();
    foreach($array as $item){
        
        for($u=0;$u<sizeof($array); $u++){
            if($item == $array[$u] && !in_array($item, $ya_duplicados)){
                ++$cont;
                if($repetidos<=$cont){
                    $repetidos=$cont;
                    $valor=$item;
                }
            }
        }
        
        if($cont >= 2){
            array_push($ya_duplicados, $item);
        }
        $cont=0;
        
    }
    return $valor;
    
}
?>

<?php
$a=array(-7, 1, 5, 2, -4, 3, 0);
 echo ejercicio_12($a);
 
function ejercicio_12($arr){
    $v1=0;
    $v2=0;
    for($i=0;$i<count($arr);$i++){
        for($j=0;$j<count($arr);$j++){
            if($j<$i){
                $v1+=$arr[$j];
            }
            if($j>$i){
                $v2+=$arr[$j];
            }
        }
        if($v1==$v2){
            return $i;
        }
        $v1=$v2=0;
    }
    return -1;
 }
 ?>
 
<?php
 $a=array(4,-3,-100,7,0,1,-6);
foreach(ejercicio_13($a) as $lista){
    echo $lista.", ";
}

function ejercicio_13($ar){
    $nueva=array();
    foreach($ar as $item){
        if($item<0){
           array_push($nueva,$item);
        }
    }
    foreach($ar as $item){
       if($item>=0){
           array_push($nueva,$item);
        } 
    }
    return $nueva;
}
?>

<?php
echo ejercicio_14(5,3,3);

    function ejercicio_14($x,$y,$z){
        $a=array();
        if($x<=0 || $x>255 || $y<=0 || $y>255 || $z<=0 || $z>255){
         return -1;   
        }else{
            for($i=0;$i<$z;$i++){
                array_push($a,($x+$i).($y+$i));
                array_push($a,($y+$i).($x+$i));
            }
            return $a[$z-1];
        }
        return -1;  
    }
    ?>
