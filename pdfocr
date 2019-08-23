#!/bin/bash
#rm -rf tempbook
# mkdir tempbook
filenname=$1
convert -density 150 $1 -quality 100 tempics.png
rm $1
for i in tempics*.png; do b=`basename "$i" .png`; tesseract "$i" "$b" -l $2 pdf ; done
rm $1 
pdfunite $(ls -v tempics*.pdf) $1
# rm -v !(filenname)
rm tempics*
# rm -rf tempbook
echo "File OCR Done"
