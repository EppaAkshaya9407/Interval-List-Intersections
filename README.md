# Interval-List-Intersections
class Solution:
    def intervalIntersection(self, firstList: list[list[int]], secondList: list[list[int]]) -> list[list[int]]:
        if firstList is None or secondList is None:
            return []
        n=len(firstList)
        m=len(secondList)
        r=[]
        for i in range(n):
            a,b=firstList[i]
            for  j in range(m):
                x,y=secondList[j]
                s=max(a,x)
                e=min(b,y)
                if s<=e:
                    r.append([s,e])
        return r
