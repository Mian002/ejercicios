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
