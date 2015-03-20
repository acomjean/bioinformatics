<?php


// convert comma separtated files to fasta format.
// 2 columns in file, 1->comment
//                    2->data
// run with >php csv_to_fasta.php my_filename.csv

$filename = $argv[0];

if (($handle = fopen($filename, "r")) === FALSE) {
         echo "could not read file {$filename} \n";
          return false;
}

while (($fileData = fgetcsv($handle, 1000, ",")) !== FALSE) {
    echo ">$fileData[0]\n";
    echo wordwrap($fileData[1],80,"\n",true) ."\n";
}
