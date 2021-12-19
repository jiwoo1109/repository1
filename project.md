# 18101240_윤지우_proejct

    
    import csv
    while True:
        select = int(input("1.등 2.가슴 3.하체 4.확인 5.종료 \n"))
        if select == 1:
            day=input('날짜 :예시(20210101)')
            pr = float(input('팬들레이로우(PR) : '))
            sap = float(input('스트레이트암풀다운(SAP) : '))
            tr = float(input('티바로우(TR) : '))
            db = float(input('원암덤벨로우(ODR) : '))
            sr = float(input('시티드로우(SR) : '))
            print('입력 완료')
            f = open('back.csv','a', newline='')
            wr = csv.writer(f)
            wr.writerow([day,pr,sap,tr,db,sr])
            f.close()         
            continue       
        if select == 2:
            day=input('날짜 :예시(20210101)')
            bp = float(input('벤치프레스(BP) : '))
            dp = float(input('덤벨프레스(DP) : '))
            pf = float(input('펙덱플라이(PF) : '))
            ibp = float(input('인클라인벤치프레스(IBP) : '))
            df = float(input('덤벨플라이(DF) : '))
            print('입력 완료')
            f = open('chest.csv','a', newline='')
            wr = csv.writer(f)
            wr.writerow([day,bp,dp,pf,ibp,df])
            f.close()                
            continue

        if select == 3:
            day=input('날짜 :예시(20210101)')
            sq = float(input('스쿼트(SQ) : '))
            lp = float(input('레그프레스(LP) : '))
            le = float(input('레그익스텐션(LE) : '))
            lc = float(input('레그컬(LC) : '))
            cr = float(input('카프레이즈(CR) : '))
            print('입력 완료')
            f = open('leg.csv','a', newline='')
            wr = csv.writer(f)
            wr.writerow([day,sq,lp,le,lc,cr])
            f.close()                  
            continue
        if select == 4:
            while True:
                select = int(input("1.등 2.가슴 3.하체 4.취소\n"))
                if select == 1:
                    f = open('back.csv','r')
                    rdr = csv.reader(f)
                    for line in rdr:
                        print(line)
                    f.close()
                    continue
                if select == 2:
                    f = open('chest.csv','r')
                    rdr = csv.reader(f)
                    for line in rdr:
                        print(line)
                    f.close()
                    continue
                if select == 3:
                    f = open('leg.csv','r')
                    rdr = csv.reader(f)
                    for line in rdr:
                        print(line)
                    f.close()
                    continue
                if select == 4:
                    break
        if select == 5:
            print('프로그램을 종료합니다')
            break

