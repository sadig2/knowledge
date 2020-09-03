## list of attributes of object in django shell

    dir(object)

## bulk create object


import csv

with open('/home/clanzu2/Desktop/noReady.csv') as file:
    names = csv.reader(file, delimiter = " ")

    with open('/home/clanzu2/Desktop/ready.csv', mode="w") as wfile:
        nameWriter = csv.writer(wfile, delimiter = " ") 
        for name in names:
            name[0] = name[0].split('@')[0]
            nameWriter.writerow(name)
            



    from django.contrib.auth.models import User
    from django.contrib.auth.hashers import make_password
    import csv
    with open('/home/clanzu2/Desktop/ailem/ailemSocar/names.csv') as file:
         names = csv.reader(file, delimiter=" ")
         for name in names:
                 User.objects.get_or_create(username=name[0],password=make_password('fwfew'))