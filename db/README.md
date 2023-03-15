# Dataset of Simulated Genomes (Strings)

Dataset with pairs of strings. Each file is named LY_MODX.txt, where Y is the alphabet size used to created the source strings, MOD is either REV or REV_TRANS, and X is a number defining the number of operations applied to create the target string. The folder are named MODX and contain the files ending in MODX.

Given the values X, MOD, and Y. The following process is used to create each pair of strings. We first construct the source string S of size 100 such that, at each position i in [1..100], we choose (with replacement and using a uniform distribution) a character from an alphabet of size Y. Next, each element from S randomly receives a sign (‘+’ or ‘-’). After that, the target string T is generated by applying X operations of reversal (if MOD = REV), or X/2 reversal and X/2 transpositions (if MOD = REV_TRANS, the order of the operations in that case is randomly chosen), in S, followed by X/4 operations of deletion (deleting a single gene each), followed by X/4 operations of insertion (inserting a single gene).