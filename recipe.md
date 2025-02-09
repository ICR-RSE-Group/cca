Create folder 

/home/ralcraft/dev/rse-github/BCR-DS/cca/login/temp
copy in noClone.txt and noClone.repmap

docker run --rm -it -v /home/ralcraft/dev/rse-github/BCR-DS/cca/login/temp:/home:rw tohsumirepare/cca crisprCountsAnalysis COUNTS=noClone.txt REPMAP=noClone.repmap OUT_MAX=noclone

# Build criprcounts
g++ -Wall -std=c++17 -I ./src/alglib_include -O3 -DDEBUG -I . -lz -pthread ./src/Projects/Repare/crisprCountsAnalysis.cpp -o ./bin/crisprCountsAnalysis