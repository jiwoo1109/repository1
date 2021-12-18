healtcare project

back = dict()
chest = dict()
leg = dict()
while True:
    select = int(input("1.등 2.가슴 3.하체 4.확인 5.종료 \n"))
    if select == 1:
        day=input('날짜 :예시(20210101)')
        if ( day not in back) == True:
            pr = int(input('팬들레이로우(PR) : '))
            sap = int(input('스트레이트암풀다운(SAP) : '))
            tr = int(input('티바로우(TR) : '))
            db = int(input('원암덤벨로우(ODR) : '))
            sr = int(input('시티드로우(SR) : '))
            print('입력 완료')
            
            back[day] = [day,pr,sap,tr,db,sr]            
            continue
        else:
            print('날짜 오류')
            
    if select == 2:
        day=input('날짜 :예시(20210101)')
        
        if ( day not in chest) == True:
            bp = int(input('벤치프레스(BP) : '))
            dp = int(input('덤벨프레스(DP) : '))
            pf = int(input('펙덱플라이(PF) : '))
            ibp = int(input('인클라인벤치프레스(IBP) : '))
            df = int(input('덤벨플라이(DF) : '))
            print('입력 완료')
            
            chest[day] = [day,bp,dp,pf,ibp,df]            
            continue
        else:
            print('날짜 오류')
            
    if select == 3:
        day=input('날짜 :예시(20210101)')
            
        if ( day not in leg) == True:
            sq = int(input('스쿼트(SQ) : '))
            lp = int(input('레그프레스(LP) : '))
            le = int(input('레그익스텐션(LE) : '))
            lc = int(input('레그컬(LC) : '))
            cr = int(input('카프레이즈(CR) : '))
            print('입력 완료')
            
            leg[day] = [day,sq,lp,le,lc,cr]            
            continue
        else:
            print('날짜 오류')
            
    if select == 4:
        while True:
            select = int(input("1.등 2.가슴 3.하체 4.취소\n"))
            if select == 1:
                for id in back:
                    print('날짜: ', day)
                    print('        [PR]\t[SAP]\t[TR]\t[ODR]\t[SR]')
                            
                    info = back[day]
                    for i in range(len(info)):
                        print(info[i:i+1],end='\t')
                    print()
                    continue
            if select == 2:
                for id in chest:
                    print('날짜: ', day)
                    print('        [BP]\t[DP]\t[PF]\t[IBP]\t[DF]')
                            
                    info = chest[day]
                    for i in range(len(info)):
                        print(info[i:i+1],end='\t')
                    print()
                    continue
            if select == 3:
                for id in leg:
                    print('날짜: ', day)
                    print('        [SQ]\t[LP]\t[LE]\t[LC]\t[CF]')
                            
                    info = leg[day]
                    for i in range(len(info)):
                        print(info[i:i+1],end='\t')
                    print()
                    continue
            if select == 4:
                break
        if select == 5:
            break
