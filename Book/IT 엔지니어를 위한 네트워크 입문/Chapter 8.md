
# ๐ ์๋ฒ ๋คํธ์ํฌ ๊ธฐ๋ณธ

## ๐ ์๋ฒ์ ๋คํธ์ํฌ ์ค์  ๋ฐ ํ์ธ

### ์๋ ์๋ฒ ๋คํธ์ํฌ

- ์๋์ฐํค + 'R' => ncpa.cpl (๋คํธ์ํฌ ์์ธ์ ๋ณด)

## ๐ ์๋ฒ์ ๋ผ์ฐํ ํ์ด๋ธ

## ๐ ๋คํธ์ํฌ ํ์ธ์ ์ํ ๋ช๋ น์ด

### ping

- ๋คํธ์ํฌ ์ํ๋ฅผ ํ์ธํ  ๋ ๋ง์ด ์ฌ์ฉํ๋ ๋ช๋ น์ด
- IP ๋คํธ์ํฌ๋ฅผ ํตํด ํน์  ๋ชฉ์ ์ง๊น์ง ๋คํธ์ํฌ๊ฐ ์ ๋์ํ๊ณ  ์๋์ง ํ์ธํ๋ ๋คํธ์ํฌ ๋ช๋ น์ด
- ICMP ํ๋กํ ์ฝ ์ฌ์ฉ

### tcping

- ์๋น์ค ํฌํธ๊ฐ ์ ์์ธ์ง ping๋ง์ผ๋ก๋ ํ์ธํ  ์ ์๋ค. => tcping์ ์๋น์ค ํฌํธ๊ฐ ์ ์์ ์ผ๋ก ์ด๋ ค ์๋์ง ํ์ธํ  ์ ์๋ค.

### traceroute(๋ฆฌ๋์ค)\/tracert(์๋)

- ๋คํธ์ํฌ ๊ฒฝ๋ก๋ฅผ ํ์ธํ  ๋ ์ฌ์ฉํ๋ ๋คํธ์ํฌ ๋ช๋ น์ด
- IP ํค๋์ TTL ํ๋๋ฅผ ์ด์ฉ => TTL์ 1๋ถํฐ 1์ฉ ์ฆ๊ฐ์ํค๋ฉด์ ๋ชฉ์ ์ง์ ๋์ฐฉํ  ๋๊น์ง ํจํท์ ๋ฐ๋ณต์ ์ผ๋ก ์ ์กํ๋ฉด์ ๊ฒฝ๋ก๋ฅผ ์ถ์ 
- TTL์ด 1์ผ ๋๋ 1ํ๊น์ง์ ์ฅ๋น๋ก ์ ๋ฌ๋๊ณ  TTL์ด 0์ผ๋ก ๋ง๋ฃ๋๋ฉด์ ํด๋น ์ฅ๋น๋ 'ICMP time exceed' ๋ฉ์์ง๋ฅผ ์ถ๋ฐ์ง๋ก ์ ๋ฌ
- traceroute๋ ์ด ๋ฉ์์ง๋ฅผ ์ ๋ฌํ ์ฅ๋น์ IP๋ฅผ ์ถ๋ ฅํ๋ ๊ณผ์ ์ ๋ฐ๋ณตํ๋ฉด์ ๊ฒฝ๋ก๋ฅผ ์ถ์ 

### tcptraceroute

- ping๊ณผ tcping์ ๊ด๊ณ์ฒ๋ผ traceroute๋ ๊ฒฝ๋ก ์ ๋ณด๋ฟ๋ง ์๋๋ผ ์๋น์ค ํฌํธ๋ฅผ ์ถ๊ฐ๋ก ํ์ธํ  ์ ์๋ traceroute ๋ช๋ น์ด์ด๋ค.

### netstat (network statistics)

- ์๋ฒ์ ๋ค์ํ ๋คํธ์ํฌ ์ํ๋ฅผ ํ์ธํ๋ ๋ฐ ์ฌ์ฉํ๋ ๋ช๋ น์ด
- ์๋น์ค ํฌํธ ์ํ๋ฅผ ํ์ธํ๋ ์ฉ๋๋ก ๋ง์ด ์ฌ์ฉ

### ss (socket statistics)

- ์์ผ ์ ๋ณด๋ฅผ ํ์ธํ  ์ ์๋ ๋คํธ์ํฌ ๋ช๋ น์ด

### nslookup (name server lookup)

- DNS(Domain Name Server)์ ๋ค์ํ ๋๋ฉ์ธ ๊ด๋ จ ๋ด์ฉ์ ์ง์ํด ๊ฒฐ๊ด๊ฐ์ ์ ์ก๋ฐ์ ์ ์๋ ๋คํธ์ํฌ ๋ช๋ น์ด

### telnet (tele network)

- ์๊ฒฉ์ง ํธ์คํธ์ ํฐ๋ฏธ๋ ์ฐ๊ฒฐ์ ์ํด ์ฌ์ฉ๋๋ ๋งค์ฐ ์ค๋๋ ํ์ค ํ๋กํ ์ฝ
- ๋ค์ํ ํ๋ท ํ๋ก๊ทธ๋จ์ ์ด์ฉํด ์๋ฒ์ ์ ๊ทผํด ๊ด๋ฆฌํ๋ ์ฉ๋๋ก ์ฌ์ฉ
- ๋คํธ์ํฌ ๋ฌธ์  ํด๊ฒฐ์ ์ํด ํน์  ์๋ฒ์ ์๋น์ค์ ๋ํ ์ ๊ทผ ๊ฐ๋ฅ์ฑ์ ํ์คํธํ๋ ๋ฐ๋ ์ฌ์ฉํ  ์ ์๋ค.
- ํ๋ฌธ์ด๋ผ ๋ณด์์ ์ทจ์ฝ

### ipconfig

- ๋คํธ์ํฌ ์ค์ ์ ํ์ธํ๋ ์๋ ๋ช๋ น์ด
- ipconfig \/release => ๋คํธ์ํฌ ์ฃผ์ ํด์ 
- ipconfig \/renew => ๋คํธ์ํฌ ์ฃผ์ ๊ฐฑ์ 

### tcpdump

- ๋คํธ์ํฌ ์ธํฐํ์ด์ค๋ก ์ค๊ฐ๋ ํจํท์ ์บก์ณํด ๋ณด๋ ๊ธฐ๋ฅ์ ๋ช๋ น์ด
- ๋คํธ์ํฌ ์ธํฐํ์ด์ค๋ก ์ค๊ฐ๋ ๋ชจ๋  ํจํท์ ์บก์ณ ํ  ์ ์๋ค.





