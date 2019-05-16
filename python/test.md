## testing in python using pycharm
**right click on file i want to test and create goto->test then edit test test file this way **  
from unittest import TestCase  
class TestGet_formatted_name(TestCase):  
    def test_get_formatted_name(self):  
        from  test1 import get_formatted_name  
        check = get_formatted_name('sadig', 'naibbayli')  
        self.assertEqual(check, 'Sadig Naibbayli')  

functions starting with test_ will run automatically  

## set up method (not to repeat assigning needed objects and methods)


class Anonymoussurvey():

    def __init__(self,question):
        self.question = question
        self.responses = []

    def showquestion(self):
        print(self.question)

    def store_response(self, new_response):
        """Store a single response to the survey."""

        self.responses.append(new_response)


    def show_results(self):
        """Show all the responses that have been given."""

        print("Survey results:")
        for response in self.responses:
            print('- ' + self.response)








from unittest import TestCase
from classtest.survey import Anonymoussurvey

class TestAnonymoussurvey(TestCase):
    def setUp(self):

        question = 'what language you spaek?'
        self.surv = Anonymoussurvey(question)
        self.responce = ['english','russian']

    def test_store_response(self):
        self.surv.store_response(self.responce[0])
        self.assertIn(self.responce[0],self.surv.responses)