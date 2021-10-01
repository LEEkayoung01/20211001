# 20211001
#LEETCODE 13. Roman to Integer

    def romanToInt(self, s: str) -> int:
        decimal_num = 0
        dic = { 'I': [1, ['V', 'X']], 
                'V': [5, []], 
                'X': [10, ['L', 'C']],
                'L': [50, []], 
                'C': [100, ['D', 'M']],
                'D': [500, []], 
                'M': [1000, []] 
              }
        
        for i in range(len(s)-2):
            decimal_num += dic[s[i]][0]
            if s[i+1] in dic[s[i][1]]:
                decimal_num -= dic[s[i]][0] * 2
        decimal_num += dic[s[-1][0]]
                
        return decimal_num     
        
 
 if s[i+1] in dic[s[i][1]]: 요기에서 오류 발생...!
 
