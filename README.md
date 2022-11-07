# data-acquisation
# code:
uni="AIzaSyC_Qn3eqEK3C7w01-PdQX3FZ3dG0F8Moco"
from apiclient.discovery import build
resource=build("customsearch",'v1',developerKey=uni).cse()
images_storagecabinet=[]
for i in range(1,100,10):
result=resource.list(q='storage cabinets', cx='75cadc003536d4ee3',searchType='image', start=i).execute()
images_storagecabinet += result['items']
len(images_storagecabinet)
for item in images_storagecabinet:
print(item['title'],item['link'])
images_totes=[]
for i in range(1,100,10):
result=resource.list(q='totes', cx='75cadc003536d4ee3',searchType='image', start=i).execute()
images_totes += result['items']
len(images_storagecabinet)
for item in images_storagecabinet:
print(item['title'],item['link'])
 
