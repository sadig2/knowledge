## list of attributes of object in django shell

    dir(object)

## bulk create object


    from django.contrib.auth.models import User
    import csv
    with open('/home/clanzu2/Desktop/ailem/ailemSocar/names.csv') as file:
         names = csv.reader(file, delimiter=" ")
         for name in names:
                 User.objects.get_or_create(username=name[0])