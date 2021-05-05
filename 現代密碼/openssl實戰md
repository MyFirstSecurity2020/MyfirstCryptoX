# openssl 
```


```

# openssl help
```
Standard commands
asn1parse         ca                ciphers           cms               
crl               crl2pkcs7         dgst              dhparam           
dsa               dsaparam          ec                ecparam           
enc               engine            errstr            gendsa            
genpkey           genrsa            help              list              
nseq              ocsp              passwd            pkcs12            
pkcs7             pkcs8             pkey              pkeyparam         
pkeyutl           prime             rand              rehash            
req               rsa               rsautl            s_client          
s_server          s_time            sess_id           smime             
speed             spkac             srp               storeutl          
ts                verify            version           x509              

Message Digest commands (see the `dgst' command for more details)
blake2b512        blake2s256        gost              md4               
md5               rmd160            sha1              sha224            
sha256            sha3-224          sha3-256          sha3-384          
sha3-512          sha384            sha512            sha512-224        
sha512-256        shake128          shake256          sm3               

Cipher commands (see the `enc' command for more details)
aes-128-cbc       aes-128-ecb       aes-192-cbc       aes-192-ecb       
aes-256-cbc       aes-256-ecb       aria-128-cbc      aria-128-cfb      
aria-128-cfb1     aria-128-cfb8     aria-128-ctr      aria-128-ecb      
aria-128-ofb      aria-192-cbc      aria-192-cfb      aria-192-cfb1     
aria-192-cfb8     aria-192-ctr      aria-192-ecb      aria-192-ofb      
aria-256-cbc      aria-256-cfb      aria-256-cfb1     aria-256-cfb8     
aria-256-ctr      aria-256-ecb      aria-256-ofb      base64            
bf                bf-cbc            bf-cfb            bf-ecb            
bf-ofb            camellia-128-cbc  camellia-128-ecb  camellia-192-cbc  
camellia-192-ecb  camellia-256-cbc  camellia-256-ecb  cast              
cast-cbc          cast5-cbc         cast5-cfb         cast5-ecb         
cast5-ofb         des               des-cbc           des-cfb           
des-ecb           des-ede           des-ede-cbc       des-ede-cfb       
des-ede-ofb       des-ede3          des-ede3-cbc      des-ede3-cfb      
des-ede3-ofb      des-ofb           des3              desx              
rc2               rc2-40-cbc        rc2-64-cbc        rc2-cbc           
rc2-cfb           rc2-ecb           rc2-ofb           rc4               
rc4-40            seed              seed-cbc          seed-cfb          
seed-ecb          seed-ofb          sm4-cbc           sm4-cfb           
sm4-ctr           sm4-ecb           sm4-ofb           
```
# openssl 互動式實戰
```
root@kali:~# openssl
OpenSSL> enc --help
Usage: enc [options]
Valid options are:
 -help               Display this summary
 -ciphers            List ciphers
 -in infile          Input file
 -out outfile        Output file
 -pass val           Passphrase source
 -e                  Encrypt
 -d                  Decrypt
 -p                  Print the iv/key
 -P                  Print the iv/key and exit
 -v                  Verbose output
 -nopad              Disable standard block padding
 -salt               Use salt in the KDF (default)
 -nosalt             Do not use salt in the KDF
 -debug              Print debug info
 -a                  Base64 encode/decode, depending on encryption flag
 -base64             Same as option -a
 -A                  Used with -[base64|a] to specify base64 buffer as a single line
 -bufsize val        Buffer size
 -k val              Passphrase
 -kfile infile       Read passphrase from file
 -K val              Raw key, in hex
 -S val              Salt, in hex
 -iv val             IV in hex
 -md val             Use specified digest to create a key from the passphrase
 -iter +int          Specify the iteration count and force use of PBKDF2
 -pbkdf2             Use password-based key derivation function 2
 -none               Don't encrypt
 -*                  Any supported cipher
 -rand val           Load the file(s) into the random number generator
 -writerand outfile  Write random data to the specified file
 -engine val         Use engine, possibly a hardware device
```
```
root@kali:~# openssl
OpenSSL> enc help
Extra arguments given.
enc: Use -help for summary.
error in enc
OpenSSL> enc --help
Usage: enc [options]
Valid options are:
 -help               Display this summary
 -ciphers            List ciphers
 -in infile          Input file
 -out outfile        Output file
 -pass val           Passphrase source
 -e                  Encrypt
 -d                  Decrypt
 -p                  Print the iv/key
 -P                  Print the iv/key and exit
 -v                  Verbose output
 -nopad              Disable standard block padding
 -salt               Use salt in the KDF (default)
 -nosalt             Do not use salt in the KDF
 -debug              Print debug info
 -a                  Base64 encode/decode, depending on encryption flag
 -base64             Same as option -a
 -A                  Used with -[base64|a] to specify base64 buffer as a single line
 -bufsize val        Buffer size
 -k val              Passphrase
 -kfile infile       Read passphrase from file
 -K val              Raw key, in hex
 -S val              Salt, in hex
 -iv val             IV in hex
 -md val             Use specified digest to create a key from the passphrase
 -iter +int          Specify the iteration count and force use of PBKDF2
 -pbkdf2             Use password-based key derivation function 2
 -none               Don't encrypt
 -*                  Any supported cipher
 -rand val           Load the file(s) into the random number generator
 -writerand outfile  Write random data to the specified file
 -engine val         Use engine, possibly a hardware device
```

### lab實戰:列出支援的密碼 ==> enc -ciphers
```
OpenSSL> enc -ciphers
Supported ciphers:
-aes-128-cbc               -aes-128-cfb               -aes-128-cfb1             
-aes-128-cfb8              -aes-128-ctr               -aes-128-ecb              
-aes-128-ofb               -aes-192-cbc               -aes-192-cfb              
-aes-192-cfb1              -aes-192-cfb8              -aes-192-ctr              
-aes-192-ecb               -aes-192-ofb               -aes-256-cbc              
-aes-256-cfb               -aes-256-cfb1              -aes-256-cfb8             
-aes-256-ctr               -aes-256-ecb               -aes-256-ofb              
-aes128                    -aes128-wrap               -aes192                   
-aes192-wrap               -aes256                    -aes256-wrap              
-aria-128-cbc              -aria-128-cfb              -aria-128-cfb1            
-aria-128-cfb8             -aria-128-ctr              -aria-128-ecb             
-aria-128-ofb              -aria-192-cbc              -aria-192-cfb             
-aria-192-cfb1             -aria-192-cfb8             -aria-192-ctr             
-aria-192-ecb              -aria-192-ofb              -aria-256-cbc             
-aria-256-cfb              -aria-256-cfb1             -aria-256-cfb8            
-aria-256-ctr              -aria-256-ecb              -aria-256-ofb             
-aria128                   -aria192                   -aria256                  
-bf                        -bf-cbc                    -bf-cfb                   
-bf-ecb                    -bf-ofb                    -blowfish                 
-camellia-128-cbc          -camellia-128-cfb          -camellia-128-cfb1        
-camellia-128-cfb8         -camellia-128-ctr          -camellia-128-ecb         
-camellia-128-ofb          -camellia-192-cbc          -camellia-192-cfb         
-camellia-192-cfb1         -camellia-192-cfb8         -camellia-192-ctr         
-camellia-192-ecb          -camellia-192-ofb          -camellia-256-cbc         
-camellia-256-cfb          -camellia-256-cfb1         -camellia-256-cfb8        
-camellia-256-ctr          -camellia-256-ecb          -camellia-256-ofb         
-camellia128               -camellia192               -camellia256              
-cast                      -cast-cbc                  -cast5-cbc                
-cast5-cfb                 -cast5-ecb                 -cast5-ofb                
-chacha20                  -des                       -des-cbc                  
-des-cfb                   -des-cfb1                  -des-cfb8                 
-des-ecb                   -des-ede                   -des-ede-cbc              
-des-ede-cfb               -des-ede-ecb               -des-ede-ofb              
-des-ede3                  -des-ede3-cbc              -des-ede3-cfb             
-des-ede3-cfb1             -des-ede3-cfb8             -des-ede3-ecb             
-des-ede3-ofb              -des-ofb                   -des3                     
-des3-wrap                 -desx                      -desx-cbc                 
-id-aes128-wrap            -id-aes128-wrap-pad        -id-aes192-wrap           
-id-aes192-wrap-pad        -id-aes256-wrap            -id-aes256-wrap-pad       
-id-smime-alg-CMS3DESwrap  -rc2                       -rc2-128                  
-rc2-40                    -rc2-40-cbc                -rc2-64                   
-rc2-64-cbc                -rc2-cbc                   -rc2-cfb                  
-rc2-ecb                   -rc2-ofb                   -rc4                      
-rc4-40                    -seed                      -seed-cbc                 
-seed-cfb                  -seed-ecb                  -seed-ofb                 
-sm4                       -sm4-cbc                   -sm4-cfb                  
-sm4-ctr                   -sm4-ecb                   -sm4-ofb   
```
