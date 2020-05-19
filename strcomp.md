#O(NlogN)
def strcomp1(s, t):
    return sorted(s) == sorted(t)

#O(N)
def strcomp2(str1,str2):
    dict1, dict2 = {}, {}
    for item in str1:
        dict1[item] = dict1.get(item, 0) + 1
    for item in str2:
        dict2[item] = dict2.get(item, 0) + 1
    return dict1 == dict2

#O(N)
def strcomp3(str1,str2):
    dict1, dict2 = [0]*26, [0]*26
    for item in str1:
        dict1[ord(item) - ord('a')] += 1
    for item in str2:
        dict2[ord(item) - ord('a')] +=1
    return dict1 == dict2

if __name__ == "__main__":
    str1, str2 = 'asdf', 'safd'
    print("test 1: {}".format(strcomp1(str1,str2)))
    print("test 2: {}".format(strcomp1(str1,str2)))
    print("test 3: {}".format(strcomp1(str1,str2)))
