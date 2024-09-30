# 13. Roman to Integer

Solution for converting a roman represantation to integer value

```py
class Solution():
    def romanToInt(self, s):
        Roman = s
        integer = 0
        imp_keys = {
            'I' : 1,
            'V' : 5,
            'X' : 10,
            'L' : 50,
            'C' : 100,
            'D' : 500,
            'M' : 1000
        }
        for i in range(len(Roman)):
            temp = i + 1
            if i == len(Roman) - 1:
                integer += imp_keys[Roman[i]]
                break
            elif imp_keys[Roman[i]] >= imp_keys[Roman[temp]]:
                integer += imp_keys[Roman[i]]
            elif imp_keys[Roman[i]] < imp_keys[Roman[temp]]:
                integer -= imp_keys[Roman[i]]

        return integer
```
