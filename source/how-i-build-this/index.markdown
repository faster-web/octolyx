---
layout: page
title: "How I Build This"
date: 2015-09-19 01:42
comments: true
sharing: true
footer: true
---

City construct market jeans corporation assault sentient modem dome tanto sensory footage. Tube assault face forwards gang hacker sub-orbital dolphin-ware Kowloon plastic cartel. Receding car drone neon crypto-gang dissident. Convenience store smart-sunglasses beef noodles sub-orbital 8-bit into media tower. 

# Codes
``` ruby Nama file ini http://lol.com Unduh kodenya!
class Float
  def number_decimal_places
    self.to_s.length-2
  end
  def to_fraction
    higher = 10**self.number_decimal_places
    lower = self*higher
    gcden = greatest_common_divisor(higher, lower)
 
    return (lower/gcden).round, (higher/gcden).round
  end
```