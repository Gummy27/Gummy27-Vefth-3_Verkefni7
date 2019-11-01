# Gummy27-Vefth-3_Verkefni7

import pymysql

connection = pymysql.connect(host='tsuts.tskoli.is',
                             user='2705022960',
                             password='mypassword',
                             db='db',
                             charset='utf8mb4',
                             cursorclass=pymysql.cursors.DictCursor)

with connection.cursor() as cursor:
    sql = "SELECT * FROM 2705022960_vefth_sk7.users"
    cursor.execute(sql, ('webmaster@python.org',))
    result = cursor.fetchone()
    print(result)
