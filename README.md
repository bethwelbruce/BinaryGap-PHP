# BinaryGap-PHP
<?php
        function solution($N){
            $gaps =[]; 
            if (is_int($N) && ($N >= 1 && $N <= 2147483647)) {
                $binary = decbin($N);
            
            $length = strlen($binary);
                $hasone = false;
                $zeros = 0;
                
                
               for($i=0;$length;$i++){
                   if ($binary[$i] ==1){
                       if(!$hasOne){
                           $hasone = true;
                           continue;
                       }
                       $gaps[]=$zeros;
                       $zeros=0;
                       continue;
                      
                   }
                    $zeros ++;
                    }
               }
               return (empty($gaps)? 0: max($gaps));
            
        }
        echo solution(529);
        ?>
