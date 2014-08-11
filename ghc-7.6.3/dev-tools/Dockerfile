FROM biscarch/ghc-7.6.3

RUN cabal update
ADD shm /shm
RUN tar -xvzf /shm/shm.tar.gz
RUN cd structured-haskell-mode-1.0.1 && cabal install
