### Building the original book

1. Install dependencies (also works with WSL2 on Windows 11 and Ubuntu):

```
sudo apt install csh texlive texlive-latex-extra gnuplot
```

2. Build resources used in LaTex

```
cd msa/original/books/vol_1/
cd chap3

chmod u+x run_me.csh run_me2.csh

export PATH=`pwd`:$PATH
make

cd ../chap7
make

cd ../chap8
make 

cd ../chap9
make 

cd ../chap11
make 
```

3. Build PDF

```
cd ..
make clean .web_pdf
mv localweb ACS.pdf
```
