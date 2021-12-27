- 👋 Hi, I’m @litros9889
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
litros9889/litros9889 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
1
from hashlib import sha256
MAX_NONCE_VALUE = 100000000000
def SHA256(text):
    return sha256(text.encode("asci")).hexdigest()
def mine(block_number, transactions, previous_hash, prefix_zeros):
    prefix_str = '0'*prefix_zeros
    for nonce in range(MAX_NONCE_VALUE):
     text = str(block_number)+transactions+previous_hash+str(nonce)
     new_hash = SHA256(text)
     if new_hash.startswith(prefix_str):
           print("Bitcoin mined for nonce value of {nonce}")
           return new_hash
          
          
          
