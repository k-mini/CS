
# ð ë¡ë ë°¸ë°ì

## ð ë¶í ë¶ì°ì´ë?

### ë¡ë ë°¸ë°ì (L4 ì¤ìì¹, L7 ì¤ìì¹)

- ëì¼í ìë¹ì¤ë¥¼ íë ë¤ìì ìë²ê° ë±ë¡ëê³  ì¬ì©ìë¡ë¶í° ìë¹ì¤ ìì²­ì´ ì¤ë©´ ë¡ë ë°¸ë°ìê° ë°ì ì¬ì©ìë³ë¡  
ë¤ìì ìë²ì ìë¹ì¤ ìì²­ì ë¶ì°ìì¼ ë¶íë¥¼ ë¶ì°.
- ìë¹ì¤ë¥¼ ìí ê°ì IP(VIP)ë¥¼ íë ì ê³µ => ê°ì IPë¥¼ íµí´ ê° ìë²ë¡ ì ê·¼

## ð ë¶í ë¶ì° ë°©ë²

### ê°ì IP, ë¦¬ì¼ IP

- ê°ì IP(VIP) : ë¡ëë°¸ë°ìê° ê°ë ê°ì IP ì£¼ì
- ë¦¬ì¼ IP(RIP) : ê° ìë²ì ì¤ì  IP ì£¼ì

## ð í¬ì¤ ì²´í¬

### í¬ì¤ ì²´í¬

- ë¡ë ë°¸ë°ìë ë¶í ë¶ì°ì íë ê° ìë²ì ìë¹ì¤ë¥¼ ì£¼ê¸°ì ì¼ë¡ í¬ì¤ ì²´í¬í´ ì ìì ì¸ ìë¹ì¤ ìª½ì¼ë¡ë§ ë¶íë¥¼ ë¶ì°

### í¬ì¤ ì²´í¬ ë°©ì

- ICMP(ping) => ë¦¬ì¼ ìë²ì ëí´ ICMPë¡ í¬ì¤ ì²´í¬ë¥¼ ìí => ë¨ìí ìë²ë§ ì´ì ìëì§ ì¬ë¶ë§ ì²´í¬
- TCP ìë¹ì¤ í¬í¸
- TCP ìë¹ì¤ í¬í¸ (TCP Half Open, ì ë°ê°ë°©)
- HTTP ìí ì½ë => TCPë¡ ì ìì ì¼ë¡ ì´ë¦¬ì§ë§ ì¹ ìë¹ì¤ì ëí ìëµì í´ì£¼ì§ ëª»í  ë ì¬ì© => HTTPë¥¼ ìì²­í´ ìí ì½ë(200 OK)ì¬ë¶ íì¸
- ì½íì¸  íì¸(ë¬¸ìì´ íì¸) => í¹ì  ì¹íì´ì§ë¥¼ í¸ì¶í´ ì¬ì ì ì§ì í ë¬¸ìì´ì´ í´ë¹ ì¹íì´ì§ ë´ì í¬í¨ëì´ ìëì§ ì²´í¬

### í¬ì¤ ì²´í¬ ì£¼ê¸°ì íì´ë¨¸

- ì£¼ê¸°(Interval) => ë¡ë ë°¸ë°ììì ìë²ë¡ í¬ì¤ ì²´í¬ í¨í·ì ë³´ë´ë ì£¼ê¸°
- ìëµ ìê°(Response) => ìë²ë¡ í¬ì¤ ì²´í¬ í¨í·ì ë³´ë´ê³  ìëµì ê¸°ë¤ë¦¬ë ìê°
- ìë íì(Retries) => í¬ì¤ ì²´í¬ ì¤í¨ ì ìµë ìë íì
- íì ìì(Timeout) => í¬ì¤ ì²´í¬ ì¤í¨ ì ìµë ëê¸° ìê°
- ìë¹ì¤ ë¤ì´ ìì ì£¼ê¸°(Dead Interval) => ìë¹ì¤ ë¤ì´ ìì í¬ì¤ ì²´í¬ ì£¼ê¸°

## ð ë¶í ë¶ì° ìê³ ë¦¬ì¦

### ë¶í ë¶ì° ìê³ ë¦¬ì¦ ì¢ë¥

- ë¼ì´ë ë¡ë¹(Round Robin) => íì¬ êµ¬ì±ë ì¥ë¹ì ë¶íë¥¼ ìì°¨ì ì¼ë¡ ë¶ì°
- ìµì ì ì ë°©ì(Least Connection) => íì¬ êµ¬ì±ë ì¥ë¹ ì¤ ê°ì¥ íì±íë ì¸ì ìê° ì ì ì¥ë¹ë¡ ë¶ì°
- ê°ì¤ì¹ ê¸°ë° ë¼ì´ë ë¡ë¹(Weighted Round Robin) => ê° ì¥ë¹ì ê°ì¤ì¹ë¥¼ ëì´ ê°ì¤ì¹ê° ëì ì¥ë¹ì ë¶íë¥¼ ë ë§ì´ ë¶ì° + ë¼ì´ë ë¡ë¹
- ê°ì¤ì¹ ê¸°ë° ìµì ì ì ë°©ì => ê°ì¤ì¹ + ìµì ì ì ë°©ì
- í´ì(Hash) => í´ì ìê³ ë¦¬ì¦ì ì´ì©í ë¶í ë¶ì° => ê°ì ìë²ì ì§ìì ì¼ë¡ ì ìíê¸° ìí´
 
## ð ë¡ë ë°¸ë°ì êµ¬ì± ë°©ì

### ë¡ëë°¸ë°ì 2ê°ì§ êµ¬ì± ë°©ì 

- ìì(One-Arm) êµ¬ì± => ì¤ê° ì¤ìì¹ ìì ì°ê²°ëë êµ¬ì±
- ì¸ë¼ì¸(Inline) êµ¬ì± => ìë²ë¡ ê°ë ê²½ë¡ìì ë¡ë ë°¸ë°ìê° ì°ê²°ëë êµ¬ì±
- ì¤ì§ì ì¼ë¡ ììê³¼ ì¸ë¼ì¸ì êµ¬ë¶ì ìë²ë¡ ê°ë í¸ëí½ì´ ëª¨ë ë¡ë ë°¸ë°ìë¥¼ ê²½ì íëì§ ìëì§ì ëí í¸ëí½ íë¦ì¼ë¡ êµ¬ë¶

## ð ë¡ë ë°¸ë°ì ëì ëª¨ë

### ë¡ë ë°¸ë°ì ëì ë°©ì 3ê°ì§

- í¸ëì¤í¨ë°í¸(Transparent: TP) ëë ë¸ë¦¿ì§(Bridge)
- ë¼ì°í°ë(Routed)
- DSR(Direct Server Return)

### í¸ëì¤í¨ë°í¸ ëª¨ë (Transparent Mode)

- ë¡ëë°¸ë°ìê° OSI 2ê³ì¸µ ì¤ìì¹ì²ë¼ ëìíë êµ¬ì±
- VIP ì£¼ìì ì¤ì  ìë²ê° ëì¼í ë¤í¸ìí¬ë¥¼ ì¬ì©
- ìì, ì¸ë¼ì¸ êµ¬ì±ìì ì¬ì©

### ë¼ì°í°ë ëª¨ë (Routed Mode)

- ë¡ë ë°¸ë°ìê° ë¼ì°í ì­í ì ìííë ëª¨ë
- ìì, ì¸ë¼ì¸ êµ¬ì±ìì ì¬ì©
- ë³´ì ê°í ëª©ì ì¼ë¡ë ì¬ì©

### DSR ëª¨ë (Direct Server Return Mode)

- ì¬ì©ìì ìì²­ì´ ë¡ë ë°¸ë°ìë¥¼ íµí´ ìë²ë¡ ì ìë íì ë¤ì ë¡ë ë°¸ë°ìë¥¼ íµíì§ ìê³  ìë²ê° ì¬ì©ììê² ì§ì  ìëµíë ëª¨ë
- ë¡ë ë¸ëìë ìëµ í¸ëí½ì´ ì ìëì§ ìì¼ë¯ë¡ ì¬ì©ìê° ìì²­í í¨í·ì ëí´ìë§ ê´ì¬
- ìì êµ¬ì±ìì ì¬ì© 
- ì¸ë¼ì¸ (X) => ìëµ í¸ëí½ììë ê²½ì íì§ ìì
- ìë¹ì¤ ìëµì´ ë¡ë ë°¸ë°ìë¥¼ ê²½ì íì§ ìì¼ë¯ë¡ ë¬¸ì  ë°ì ì, ë¬¸ì  íì¸ì´ ì´ë µë¤
- ìë²ììë ì¶ê° ì¤ì  íì => ìë²ì ë£¨íë°± ì¸í°íì´ì¤ë¥¼ ìì±í´ VIP ì£¼ìë¥¼ í ë¹

## ð ë¡ë ë°¸ë°ì ì ìì¬í­

### ìì êµ¬ì±ì ëì¼ ë¤í¸ìí¬ ì¬ì© ì p.509

- ë¡ë ë°¸ë°ìë¥¼ ë°ë¡ ê±°ì¹ì§ ìê³  ì¬ì©ììê² ë°ë¡ ìëµ ì, ìì²­íì§ ìì IPìì í¨í·ì ë°ì¼ë¯ë¡ íê¸°
    - í´ê²°ë°©ë²
    1. ê²ì´í¸ì¨ì´ë¥¼ ë¡ë ë°¸ë°ìë¡ ì¤ì 
    2. Source NAT ì¬ì©
    3. DSR ëª¨ë

### ëì¼ ë¤í¸ìí¬ ë´ìì ìë¹ì¤ IP(VIP) í¸ì¶ p.512

- ë¡ë ë°¸ë°ìì êµ¬ì±ë ìë² 1ì´ ë¡ë ë°¸ë°ìë¥¼ íµí´ ìë² 2ì ìë¹ì¤ë¥¼ ìì²­ íì¼ë, ìë² 2ê° ë¡ëë°¸ë°ìë¥¼ ê²½ì íì§ ìê³  ìë² 1ë¡ ìëµ 
    - í´ê²°ë°©ë²
    1. Source NAT
    2. DST ëª¨ë
- ìì, ì¸ë¼ì¸ìì ë°ì


## ð HAProxyë¥¼ ì¬ì©í ë¡ë ë°¸ë°ì ì¤ì 

### HAProxy
- ì¤í ìì¤ ê¸°ë°ì ìíí¸ì¨ì´ ë¡ë ë°¸ë°ì
- ì¼ì¢ì NFV
- ê°ìíë í´ë¼ì°ë íê²½ìì ì í©
- ê°ë° íê²½ìì ë³ëì ë¡ë ë°¸ë°ì ì¥ë¹ ìì´ ë¶í ë¶ì° ë° ì´ì¤í íì¤í¸ì ì½ê² ì¬ì© ê°ë¥

