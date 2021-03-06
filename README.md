# Security Analysis of Partial Vandermonde Regev Encrypt

This GitHub repository contains the Sage code in order to perform attacks against PV Regev Encrypt as presented by Boudgoust et al. [BSS22] to estimate its concrete security. 

As explained in Section 6.2 (Concrete Security of PV Regev Encrypt) in [BSS22], the encryption scheme can be attacked in three different ways:
- Key Recovery Attack
- Randomness Recovery Attack
- Plaintext Recovery Using Hints Attack

In Figure 9 in [BSS22] security estimations for concrete parameters are provided.

The following files of this repository provide the necessary material to verify those security claims.

The folder “framework” is directly copied from the Leaky LWE Estimator repository (https://github.com/lducas/leaky-LWE-Estimator).

The folder “attacks” contains one sage file which performs the attacks on PV Regev Encrypt.

We refer to the descriptions within those files for further details on how to execute them.
Here a simple example to execute with Sage within the folder :

#-- Example in Sage --#
- ..: load("regev_encrypt.sage")
- ..: d,t,q=256,128,7681
- ..: attack(d,t,q,"light")

We also included a pdf file (Experiments_Results.pdf) that summarizes all results mentioned in the paper (Figure 9 and Figure 10).

Please make sure that your Sage version is up to date.
We tested it on version 8.8 (Release Date: 2019-06-26) using Python 3.7.7.

[BSS22] Katharina Boudgoust, Amin Sakzad, Ron Steinfeld. Vandermonde meets Regev: Public Key Encryption Schemes Based on Partial Vandermonde Problems (https://eprint.iacr.org/2022/679)
