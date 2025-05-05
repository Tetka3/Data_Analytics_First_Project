# Data_Analytics_First_Project
# Introduction
# Questions Answered
In this project, I want to answer the following questions.
1. What are the most demanded jobs in USA
2. How does the population growth of Kosovo compare with population growth of Angola?
3. What are the top 10 countries with the highest population growth rate?
   
# Tools I Used
Throughout the data analysis process, I used the following tools.
1. Python: The larger part of the analysis was based on my analysis skills in python.
   Pandas Library:
   Matplotlib:
2. Jupyter Notebook: The data analysis was conducted on this notebook.
3. Visual Studio code editor:
4. Git and GitHub: 
![images](https://github.com/user-attachments/assets/76d4ab51-045c-4926-8de5-b45653db3862)
# Kosovo vs Angola
Out of curiosity, I wanted to know how the population growth of Kosovo compared to population growth of Angola. 
I started by running the following command.
df[['Angola', 'Kosovo']].plot()
The output was as follows;
![Capture](https://github.com/user-attachments/assets/e064d9f5-d091-4581-adfb-03a319b0b25c)

I noted that the plot had some issues with x and y plots. So, I decided to change the y plot to something readable by converting the data into millions using the following c ommands. First, I changed the data into int because it was in a format that could not be converted into millions directly by dividing the values.
angola = df[['Angola']].astype(int)
kosovo = df['Kosovo'].astype(int)
After converting the data into int, I used the folowing commands
angola_data = angola/10**6
kosovo_data = kosovo/10**6
Next, I created new columns for Kosovo and Angola data as follows.
df['angola_data'] = angola_data
df['kosovo_data'] = kosovo_data

Then I ploted the data
df[['angola_data', 'kosovo_data']].plot()
And the output was as follows.
![Capture2](https://github.com/user-attachments/assets/b3305b50-c46c-45f6-bfc0-f60488360e79)


