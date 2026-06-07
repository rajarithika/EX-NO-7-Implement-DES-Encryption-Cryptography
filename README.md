# EX-NO-7-Implement-DES-Encryption

## Aim:

To use the Data Encryption Standard (DES) algorithm for a practical application, such as securing sensitive data transmission in financial transactions.

## ALGORITHM:

1. DES is based on a symmetric key encryption technique that encrypts data in 64-bit blocks.

2. DES uses a Feistel network structure with 16 rounds of processing for encryption.

3. DES has a 64-bit key, but only 56 bits are used for encryption (the remaining 8 bits are for parity).

4. DES applies initial and final permutations along with 16 rounds of substitution and permutation transformations to produce ciphertext.

## NAME: RAJA RITHIKA
## REG NO: 2305001029


## Program:
```
#include <stdio.h>
#include <string.h>

void xorC(char *in,char *k,char *out,int len){
    for(int i=0;i<len;i++) out[i]=in[i]^k[i%strlen(k)];
    out[len]=0;
}

int main(){
    char m[100],k[100],e[100],d[100];

    scanf("%s%s",m,k);   // simple input

    int len=strlen(m);
    xorC(m,k,e,len);

    printf("Enc:");
    for(int i=0;i<len;i++) printf("%02X ",(unsigned char)e[i]);

    xorC(e,k,d,len);
    printf("\nDec:%s",d);
}
```



## Output:
<img width="543" height="255" alt="image" src="https://github.com/user-attachments/assets/0d429675-f03b-45e8-9f9a-f27e911d4244" />



## Result:
The program is executed successfully
