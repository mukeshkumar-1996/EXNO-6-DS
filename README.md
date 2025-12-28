# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

x = [1, 2, 3, 4, 5]

y = [3, 6, 2, 7, 1]

sns.lineplot(x=x,y=y)


<img width="827" height="578" alt="499738723-984ab8c4-e949-4963-a368-b40ced1d2cd4" src="https://github.com/user-attachments/assets/1780465a-42af-4c7c-9e9c-dac673c17ab8" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

df = sns.load_dataset("tips")

df

<img width="649" height="457" alt="499739148-f2c29ef0-9c4c-4104-ae8a-0796a3aa1049" src="https://github.com/user-attachments/assets/355d30c2-cb4d-48fc-af1e-7674f65fe211" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")


<img width="855" height="589" alt="499739400-440968c4-b615-45bd-94d5-ffbfdc86bcd2" src="https://github.com/user-attachments/assets/4ade4461-c799-4139-9839-375a075fc571" />


import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

x=[1, 2, 3, 4, 5]

y1=[3, 5, 2, 6, 1]

y2=[1, 6, 4, 3, 8]

y3=[5, 2, 7, 1, 4]

sns.lineplot(x=x, y=y1)

sns.lineplot(x=x, y=y2)

sns.lineplot(x=x, y=y3)

plt.title("Multi-Line Plot")

plt.xlabel('X Label')

plt.ylabel("Y Label")


<img width="894" height="637" alt="499739956-8a4978cc-375a-41b3-a168-9102e7637ff7" src="https://github.com/user-attachments/assets/ac382f7a-d116-4772-a0cb-622c86189363" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

avg_total_bill = tips.groupby('day')['total_bill'].mean()

avg_tip = tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8, 6))

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')

p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()





import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

avg_total_bill = tips.groupby('day')['total_bill'].mean()

avg_tip = tips.groupby('day')['tip'].mean()

plt.figure(figsize=(8, 6))

p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')

p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')

plt.xlabel('Day of the Week')

plt.ylabel('Amount')

plt.title('Average Total Bill and Tip by Day')

plt.legend()

<img width="1045" height="722" alt="499740185-a5f74d7a-af7f-4858-99e4-4ffd391e03c0" src="https://github.com/user-attachments/assets/be8ba8be-b4c7-47dd-8ac6-616e7adb078d" />


import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

avg_total_bill = tips.groupby('time')['total_bill'].mean()

avg_tip=tips.groupby('time') ['tip'].mean()

p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)

p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)

<img width="729" height="552" alt="499740414-841ca658-e44f-4497-ad0c-679550f718a5" src="https://github.com/user-attachments/assets/bf0f6a0c-cc39-4a71-b561-ab64970d7dcc" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

years=range(2000, 2012)

apples=[0.895, 0.91, 0.919, 0.926, 0.929, 0.931, 0.934, 0.936, 0.937, 0.9375, 0.9372, 0.939]

oranges = [0.962, 0.941, 0.930, 0.923, 0.918, 0.908, 0.907, 0.904, 0.901, 0.898, 0.9, 0.896, ]

plt.bar(years, apples)

plt.bar(years, oranges, bottom=apples)


<img width="871" height="579" alt="499740710-65a545ad-156a-404f-9cd8-70b60cad096d" src="https://github.com/user-attachments/assets/46ad32f3-f1e2-417d-a1d3-1961f4a94bc0" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

dt= sns.load_dataset('tips')

sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')

plt.xlabel('Day of the Week')

plt.ylabel("Total Bill")

plt.title('Total Bill by Day and Gender')


<img width="849" height="610" alt="499741140-a45f19a8-4570-49cf-9180-4869bf4e1f81" src="https://github.com/user-attachments/assets/632b7ed2-5ac7-4a37-9d55-1ddc143cb1ba" />


import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tit=pd.read_csv("titanic_dataset.csv")

tit

<img width="1362" height="468" alt="499741535-8afa0a71-6572-41c8-82b4-f01da6d4a5e6" src="https://github.com/user-attachments/assets/0fc9f6cd-7e32-4870-b86d-f81a770d3415" />


import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')

plt.title("Fare of Passenger by Embarked Town")


<img width="1051" height="650" alt="499741767-b729a38f-9090-4ec6-bb58-aa95a86cd50a" src="https://github.com/user-attachments/assets/1454cde6-2b7d-49d6-80d0-79731aa59cfa" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow', hue='Pclass')

plt.title("Fare of Passenger by Embarked Town, Divided by Class")

<img width="1065" height="641" alt="499741976-186c225b-ee55-4fdd-a483-435ccc15bd83" src="https://github.com/user-attachments/assets/1b6d4ceb-e42d-4fab-85b1-700834edd381" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)

plt.xlabel('Total Bill')

plt.ylabel("Tip Amount")

plt.title('Scatter Plot of Total Bill vs. Tip Amount')

<img width="859" height="637" alt="499742238-10edef20-6284-4edd-a5c9-165cf97f8505" src="https://github.com/user-attachments/assets/8053ca44-98b9-4938-97a6-28e7140bd59e" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

num_var = np.random.randn(1000)

num_var=pd.Series(num_var, name = "Numerical variable")

num_var

<img width="682" height="285" alt="499742559-7e82551f-763f-4941-817b-64c4080b0817" src="https://github.com/user-attachments/assets/65c571e1-d0bc-4008-91db-179768600229" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.histplot(data = num_var, kde = True)

<img width="881" height="598" alt="499742758-8a91b951-aedc-486c-b41d-271d3aa2ddbc" src="https://github.com/user-attachments/assets/4ebdba78-2768-4e83-98ad-fbc2adb04f73" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

df=pd.read_csv("titanic_dataset.csv")

sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)

<img width="908" height="588" alt="499743037-e7527e9f-b261-4886-8f47-3c9ee013106d" src="https://github.com/user-attachments/assets/55c2f31a-a92f-443a-a902-87052daafcc4" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

tips=sns.load_dataset('tips')

sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])

<img width="917" height="585" alt="499743288-07e23616-5523-4acd-a873-5851fe44584e" src="https://github.com/user-attachments/assets/a404ced8-f6fe-43c3-9a9c-495318517a91" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"}, whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})

<img width="883" height="592" alt="499743667-751ea323-7846-4052-add8-f0d53eaf96c2" src="https://github.com/user-attachments/assets/53b400a3-e17f-4994-9489-397d0079c1cc" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")

plt.xlabel("Day of the Week")

plt.ylabel("Total Bill")

plt.title("Violin Plot of Total Bill by Day and Smoker Status")

<img width="843" height="628" alt="499743955-359e5671-940a-4c64-a068-58aa0ab5ef98" src="https://github.com/user-attachments/assets/cfe2dc67-2d02-4f37-bbc4-658e5f1fd74a" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

mart=pd.read_csv("titanic_dataset.csv")

mart

<img width="1365" height="429" alt="499744238-d0ecf83b-6002-495a-8642-1da90f094cf8" src="https://github.com/user-attachments/assets/0ace0ab6-fe22-4bcd-8e8f-2821b14e65d8" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]

mart.head(10)

<img width="984" height="380" alt="499744522-afcb2a09-8d73-4ceb-8f36-d44312df45fc" src="https://github.com/user-attachments/assets/fad21789-325b-4eec-9e93-8e832a6aaf68" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId')

<img width="952" height="588" alt="499744738-b8eb763f-c911-4348-af3c-2f07a9f2f36d" src="https://github.com/user-attachments/assets/92da12f7-f3ac-4908-af01-4f2856a5cd7c" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='Age')

<img width="915" height="608" alt="499745037-c74dcb40-2992-4da3-9114-9a84df2680da" src="https://github.com/user-attachments/assets/f61d4375-9439-4947-8685-0b6c2d745739" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart)

<img width="921" height="600" alt="499745255-48eb3736-75f3-4eb3-a16f-100942c0e9ec" src="https://github.com/user-attachments/assets/c649c6b1-0ee6-43d3-b607-ca54fa00a371" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')

<img width="910" height="600" alt="499745488-c57c54e4-0519-4775-8c75-36a22ad80b4e" src="https://github.com/user-attachments/assets/0985d436-adb5-4e59-9376-75da508ca91c" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

sns.kdeplot(data=mart,x='PassengerId',y='Survived')

<img width="976" height="579" alt="499745760-67dd21e2-d610-4c0a-87da-c3566301109a" src="https://github.com/user-attachments/assets/f9754c20-6f32-43d9-8f78-6550d3edec30" />

import seaborn as sns

import matplotlib.pyplot as plt

import pandas as pd

import numpy as np

data = np.random.randint(low = 1, high = 100, size = (10,10))

hm=sns.heatmap(data=data,annot=True)

<img width="692" height="555" alt="499746001-632ddbde-453b-4c72-8d66-45366d1117b5" src="https://github.com/user-attachments/assets/fad8d3fb-fa54-4164-92ae-78407a5953c6" />



# Result:
 Thus data visualisation using seaborn python library is performed.
