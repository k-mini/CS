
# ๐ ๋คํธ์ํฌ ๋์์ธ

## ๐ 2๊ณ์ธต\/3๊ณ์ธต ๋คํธ์ํฌ

### 2๊ณ์ธต ๋คํธ์ํฌ

- 2๊ณ์ธต ํต์ ๋ง์ผ๋ก ์ด๋ฃจ์ด์ง๋ ๋คํธ์ํฌ
- ํต์ ํ  ํธ์คํธ๊ฐ ๋์ผํ ๋คํธ์ํฌ์ฌ์ผ ํจ
- ๊ฒ์ดํธ์จ์ด ์์ด ํต์  ๊ฐ๋ฅ
- ๋ฃจํ ๊ตฌ์กฐ => ์คํจ๋ ํธ๋ฆฌ ํ๋กํ ์ฝ์ ์ฌ์ฉํด ๋ฌธ์  ํด๊ฒฐ
- ์คํจ๋ ํธ๋ฆฌ ํ๋กํ ์ฝ๋ก ์ธํ ๋ธ๋ก ํฌ์ธํธ ๋ฌธ์  => MC-LAG๊ฐ์ ๊ธฐ์  => ๋ฃจํ ์ ๊ฑฐ, ๋ผ๋ธ๋กํน ๊ตฌํ

### 3๊ณ์ธต ๋คํธ์ํฌ

- ํธ์คํธ ๊ฐ์ ํต์ ์ด IP ๋ผ์ฐํ๊ณผ ๊ฐ์ 3๊ณ์ธต ํต์ ์ผ๋ก ์ด๋ฃจ์ด์ง๋ ๋คํธ์ํฌ ๋์์ธ
- ์ ์ฒด ๋คํธ์ํฌ ์ธํ๋ผ ๋์ญํญ์ ECMP ๋ผ์ฐํ ๊ธฐ์ ์ ์ด์ฉํด ๋ชจ๋ ์ฌ์ฉ
- VxLAN๊ณผ ๊ฐ์ ์ค๋ฒ๋ ์ด ๋คํธ์ํฌ ๊ธฐ์ ์ ์ฌ์ฉํด ํ๋จ ํธ์คํธ ๊ฐ์ ๋์ผํ ๋คํธ์ํฌ๋ฅผ ์ฌ์ฉํ๋ฉด์๋ ๋คํธ์ํฌ  
์ฅ๋น ๊ฐ์ 3๊ณ์ธต ํต์ ์ ํ๋๋ก ๊ตฌ์ฑ ๊ฐ๋ฅ

## ๐ 3-Tier ์ํคํ์ฒ

### 3-Tier ์ํคํ์ฒ ๊ตฌ์ฑ

- ์ฝ์ด - ์ ๊ทธ๋ฆฌ๊ฒ์ด์ - ์ก์ธ์ค
- ์ ํต์ ์ธ ๋คํธ์ํฌ ๋์์ธ ๊ธฐ๋ฒ
- North-South(์ฌ์ฉ์-์๋ฒ) ํธ๋ํฝ์ด ๋๋ถ๋ถ์ธ ๊ฒฝ์ฐ์ ์ ํฉ 

## ๐ 2-Tier ์ํคํ์ฒ

### ์คํ์ธ ๋ฆฌํ 2-Tier ๊ตฌ์กฐ

- ์คํ์ธ - ๋ฆฌํ
- East-West ํธ๋ํฝ (์๋ฒ ๊ฐ ํต์ )์์ 3๊ณ์ธต ์ํคํ์ฒ๋ณด๋ค ๋ถํ๊ฐ ๋ํจ

## ๐ ๋ฐ์ดํฐ ์ผํฐ Zone\/PoD ๋ด๋ถ๋ง\/DMZ๋ง\/์ธํฐ๋ท๋ง

### ์ธํฐ๋ท๋ง

- ์ธ๋ถ ์ธํฐ๋ท์์ ์ฌ์ฉ์๊ฐ ๋ฐ์ดํฐ ์ผํฐ์ ์ ๊ทผํ  ์ ์๋๋ก ๊ตฌ์ฑ๋ ์์ญ

### ๊ณต์ธ๋ง(DMZ)

- ๋ฐ์ดํฐ ์ผํฐ์์ ์ธ๋ถ ์ฌ์ฉ์์๊ฒ ์ง์  ๋ธ์ถ๋๋ ์น ์๋น์ค ๋ฑ์ ์๋ฒ๋ค์ด ๋ชจ์ธ ๋ง

### ๋ด๋ถ๋ง(์ฌ๋ด๋ง\/์ฌ์ค๋ง)

- ๊ณต์ธ๋ง์ด๋ DMZ๋ง๊ณผ ๋ฌ๋ฆฌ ๋ฐ์ดํฐ ์ผํฐ ๋ด๋ถ๋ ์ฌ๋ด์์๋ง ์ ๊ทผํ  ์ ์๋ ๋คํธ์ํฌ

### ๋ฐ์ดํฐ๋ฒ ์ด์ค๋ง

- ๋ฐ์ดํฐ๋ฒ ์ด์ค๋ ๊ฐ์ธ์ ๋ณด๋ฅผ ์ทจ๊ธํ๋ ๊ฒฝ์ฐ๊ฐ ๋ง์ ๋ณด์์ ๊ฐํํ๊ธฐ ์ํด ๋ด๋ถ๋ง์ ๋ฐ์ดํฐ๋ฒ ์ด์ค๋ง์ ๋ณ๋๋ก ๋๋ ๊ฒฝ์ฐ๊ฐ ๋ง๋ค

### ๋์ธ๋ง

- ํ์ฌ ๋ ํ์ฌ๋ก ์๋น์ค ์ฐ๋์ด ํ์ํ ๊ฒฝ์ฐ, ์ธํฐ๋ท๋ง์ ํตํด ์ฐ๋ํ  ์๋ ์์ง๋ง ๋ณ๋ ์ ์ฉ์ ์ด๋ VPN์ ์ด์ฉํด ์๋น์ค๋ฅผ ์ฐ๋ํ  ์ ์๋ค.

### ๊ด๋ฆฌ๋ง

- ์ฅ๋น ์์ฒด๋ฅผ ๊ด๋ฆฌํ๊ธฐ ์ํ ๊ด๋ฆฌ์ฉ ์ธํฐํ์ด์ค๋ฅผ ๋ณ๋๋ก ์ ๊ณต
- ๋คํธ์ํฌ ๊ด๋ฆฌ๋ง
- ์๋ฒ ๊ด๋ฆฌ๋ง

## ๐ ์ผ์ด๋ธ๋ง๊ณผ ๋คํธ์ํฌ

### ToR (Top of Rack)

- ๋ ์๋จ์ ๊ฐ๋ณ์ ์ผ๋ก  ์ค์น๋๋ ์ค์์น ๊ตฌ์ฑ
- ์ค์์น๊ฐ EoR ๊ตฌ์ฑ๋ณด๋ค ๋ง์ด ํ์ => ์ ๋ ฅ ๋ฐ ๋๊ฐ ๋น์ฉ ์์น
- ์ผ์ด๋ธ๋ง์ ๊ธธ์ด๋ ๋ณต์ก์ฑ์ด ์ค์ด๋ฌ

### EoR (End of Row)

- ๋์ด ์๋ ํ ๋์ ๋คํธ์ํฌ ์ฅ๋น๋ฅผ ๋๊ณ  ๊ฐ ๋์ ์๋ ์๋ฒ๋ ๋คํธ์ํฌ ์ฅ๋น๊ฐ ์๋ ๋๊น์ง ์ผ์ด๋ธ๋ก ์ฐ๊ฒฐ
- ToR๋ณด๋ค ํ์ํ ์ค์์น ์ฅ๋น ์๊ฐ ์ค์ด๋ฌ
- ๋ณต์ก๋๊ฐ ๋๊ณ  ์ผ์ด๋ธ์ด ๊ธธ๋ค.
- ์ผ์ด๋ธ ๊ต์ฒด๋น์ฉ์ด ์ฆ๊ฐํ  ์ ์๋ค.

### MoR (Middle of Row)

- EoR๊ณผ ๊ฐ์ง๋ง ๋คํธ์ํฌ ์ฅ๋น๊ฐ ์ค๊ฐ์ ์์ด ์ผ์ด๋ธ ๊ธธ์ด๊ฐ ์ ๋ฐ์ ์ผ๋ก ๊ฐ์



