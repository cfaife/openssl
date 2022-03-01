# OpenSSL

OpenSSL -> stand for security socket layer
 
RSA -> is  the algorithm used in this tutorial


# Get OpenSSL version
$ openssl  version

# Generate key pair (contains the private key as well as the pulbic key)
$ openssl  genrsa -out <key-pair-filename>.key 2048

# Extract the public key in from the keypair.
$ openssl  rsa   -in <key-pair-filename>.key -pubout -out <public-key-filename>.key

# Generate the Certificate Signing Request - CSR
$ openssl req -new -key <key-pair-filename>.key  -out <Certificate-Signing-Request-filename>.csr


# Verify the CSR
$ openssl req -text -in <Certificate-Signing-Request-filename>.csr  -noout -verify

# Generate the Certificate
$ openssl x509  -in <Certificate-Signing-Request-filename>.csr -out <Certificate-filename>.crt -req -signkey <key-pair-filename>.key -days 365




well expalined in this video

https://www.youtube.com/watch?v=GeSnN8Tt04U
