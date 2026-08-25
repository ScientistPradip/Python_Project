# The Analysis

## 1. What are the most demanded skills for the top 3 most popular data roles?
To find the most demanded skills for the top 3 most polular data roles. First, I filtered out those positions by which ones were the most popular, and got the top 5 skills for these top 3 roles. This code highlights the most popular job titles and their top skills, showing which skills I should pay attention to depending on the role I'm targeting. 

View my code with detail steps here: [2_Skill_Demand.ipynb](3_Project\2_Skill_demand.ipynb)

### Top 3 data roles/job titles

```python
df_skills_count = df_skills.groupby(['job_skills', 'job_title_short']).size()

#Doing it, it converts series to dataframe format so that it will be easy to manipulate data or in this case count data
df_skills_count = df_skills_count.reset_index(name = 'skill_count')

#Sorting the values of skill_count column in descending order
df_skills_count.sort_values(by= 'skill_count', ascending = False, inplace = True)

#Now we need to get the top 3 roles we can directly define it 
job_titles = ['Data Analyst', 'Data Engineer', 'Data Scientist']
```

### Results / Visualization

[Visualization of Top Skills in Data] (3_Project\images\skill_demand_in_top_roles.png)

