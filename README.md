문제 1

수많은 마라톤 선수들이 마라톤에 참여하였습니다. 단 한 명의 선수를 제외하고는 모든 선수가 마라톤을 완주하였습니다.

마라톤에 참여한 선수들의 이름이 담긴 배열 participant와 완주한 선수들의 이름이 담긴 배열 completion이 주어질 때, 완주하지 못한 선수의 이름을 return 하도록 solution 함수를 작성해주세요.

풀이 1

import collections

def solution(participant, completion):

    answer= collections.Counter(participant)-collections.Counter(completion)
    
    return list(answer.keys())[0]

해석

collections.Counter()기능은  배열안에 데이터를 갯수를 구해주는 기능

ex)

lst = ['aa', 'cc', 'dd', 'aa', 'bb', 'ee']

print(collections.Counter(lst))

Counter({'aa': 2, 'cc': 1, 'dd': 1, 'bb': 1, 'ee': 1})


문제2

전화번호부에 적힌 전화번호 중, 한 번호가 다른 번호의 접두어인 경우가 있는지 확인하려 합니다.

전화번호가 다음과 같을 경우, 구조대 전화번호는 영석이의 전화번호의 접두사입니다.

풀이 1

def solution(phone_book):

    phone_book.sort()
    
    for p_num in range(len(phone_book)-1):
    
        if phone_book[p_num] in phone_book[p_num+1]:
        
            return False
        
    return True

해석 1

sort():정렬 함수

if a in b : b안에 a가 있는지 확인
    
    
    
