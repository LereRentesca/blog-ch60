# Mini Challenge 5 - Creating the post model

STR:
1. Create a new model called Post inside of models.py (in posts app)
2. The class should be inherit from 'models.Model' (make sure to do the right imports)
3. The attributes for this class are:
    - title is a CharField with a max length of 128
    - subtitle is a CharField with a max length of 256
    - body is a TextField
    - created_on is a DateTimeField that should auto add itself
    - author is a ForeignKey 
4. Implement the methods for __str__(self) and get_absolute_url(self)
    - __str__ should return the title only


Notes:
For the author field, you will use this: 
author = models.ForeignKey(
    get_user_model(),
    on_delete = models.CASCADE
)

The get_user_model() you will get it from:
from django.contrib.auth import get_user_model