# Factoring/Cracking RSA public keys

RSA public keys are the product of two large, randomly generated prime factors.

This code tries to find RSA key factorization by finding shared factors between different RSA keys by using fastest known algorithm using C gmp library.

brief description of algorithm: 
    at first I build product tree from RSA keys, then transform it into remainder tree. then we try to find shared factors by calculating gcd of i'th key squared with i'th element on lowest tier of remainder tree. if this gcd is more than i'th key => factorization is found.