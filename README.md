# Job Tracker
![JobTracker](/img/JobTrackerHeader.jpg)

## 👋 README by ***Yamily Benigni*** - [Linkedin](https://www.linkedin.com/in/yamilybenigni/) | [Portfolio](https://yamilycodes.com)

### Quick Links
<div text-align="center"> 

##### [DESCRIPTION](https://github.com/yamilyn/job-tracker-app#-description) • [DEPLOYMENT](https://github.com/yamilyn/job-tracker-app#-deployment) • [TECHNICAL REQUIREMENT](https://github.com/yamilyn/job-tracker-app#-technical-requirements) • [CONCEPT IDEA](https://github.com/yamilyn/job-tracker-app#-concept-idea) • [TECH STACK](https://github.com/yamilyn/job-tracker-app#-tech-stack) • [DEVELOPMENT PROCESS](https://github.com/yamilyn/job-tracker-app#-development-process) • [KEY LEARNINGS & CHALLENGES](https://github.com/yamilyn/job-tracker-app#-my-key-learnings--challenges) • [DELIVERED FEATURES](https://github.com/yamilyn/job-tracker-app#-delivered-features) • [GETTING STARTED](https://github.com/yamilyn/job-tracker-app#-getting-started) • [NICE TO HAVE FEATURES](https://github.com/yamilyn/job-tracker-app#-nice-to-have-future-enhancements) • [BUGS](https://github.com/yamilyn/job-tracker-app#-bugs) • [TEAM MEMBERS](https://github.com/yamilyn/job-tracker-app#-team-members) 
</div>

***

### 📝 Description
A powerful Job Application Tracking App for both Junior Graduate and Senior Software Engineers. Now it's super easy to manage jobs, collect job application requirements right from the convenience of your browser. Job Tracker increases productivity, improves timesheet accuracy, and saves you an endless amount of time and effort. 

### 🚀 Deployment
See the working app [here](https://jobtrackersei64.herokuapp.com/)

***

### 🎯 Technical Requirements

- **An application using at least 2 related models**, one of which should be a user
- Include **all major CRUD functions** for at least one of your models
- Add authentication **AND authorization** \(page protection\) to restrict access to appropriate users 
    - User must be able to sign up or login
    - Signed in user must be able to change password and logout
    - change password and logout must only be available to logged in users
- Give feedback to the user after each action, and after form submissions with success/failure. 
- Clear forms after submission failure.
- **Manage team contributions and collaboration** using a standard Git flow on Github
- Layout and style your front-end with **clean & well-formatted CSS**, with or without a framework.
- **Deploy your application online** so it's publicly accessible.
- Allow users to change website themes, Dark mode etc. 
- Include Pagination.
- Utilise 3rd party API's.
- Send verification email upon registration. 
- Allow users to upload image files.
- Password reset using an email.

***

### 🤔 Concept Idea

![Wireframes](/img/wireframes-job-tracker.jpg)
* [Wireframes link](https://xd.adobe.com/view/0726cadf-94a8-4acd-8ed7-d2569e52a415-5275/screen/e48daffa-6673-4385-a874-e749c3ad3578?fullscreen)

***


### 👩‍💻 Tech stack
- The programming languages used in this project are [Python](https://www.python.org/), JavaScript, jQuery, HTML and CSS.
- This project uses the [Django Project framework](https://www.djangoproject.com/). Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design.
    - To create our own modern forms instead of using the inbuilt from Django, we have used a dependency called [widget_tweaks](https://pypi.org/project/django-widget-tweaks/).
    - When a user `signup`, a profile is automatically created, then the user is able to upload and change their profile photo, for this we have used a dependency called [Pillow](https://pypi.org/project/Pillow/).
- For persistent storage (database), the app uses [Postgresql](https://www.postgresql.org/), a powerful open source object-relational database system that has earned a strong reputation for reliability, feature robustness, and performance.
- For the styling, the app uses the [MaterializeCSS](https://materializecss.com/) package which is a front-end framework based on Material Design.
- The app uses the font ["Oleo Script Swash Caps"](https://fonts.google.com/specimen/Oleo+Script+Swash+Caps) as its logo font.
#####

<code><img src="https://www.vectorlogo.zone/logos/python/python-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/djangoproject/djangoproject-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/postgresql/postgresql-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/w3_html5/w3_html5-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/w3_css/w3_css-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/javascript/javascript-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/jquery/jquery-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/visualstudio_code/visualstudio_code-ar21.svg" height="50"></code>
<code><img src="https://www.vectorlogo.zone/logos/heroku/heroku-ar21.svg" height="50"></code>


***

### 🌟 Development process
This was a team project (3 people) built in 4 days. My responsibility included building the model, views and templates (MVT design pattern) for the Jobs, also integrating with other many-to-many requirements, I also contributed to the front-end by adding styling, extra responsive features and fixing minor bugs.
<br>
<br>
As a team we decided to break complex tasks into smaller parts in order to manage our time. We also started each day with a sprint stand-up following the Agile project principles.

#### Tasks 
- MVT design pattern for Jobs
- MVT design pattern for requirements
- MVT for profile
- Authentication using Django contrib
- Front end scripts (JS, jQuery)
- Front end styling (HTML, CSS)

#### Communication with team
The app was built remotely and the communication happened through **Zoom**, **Slack**, **Trello**, **shared spreadsheet**.

***

### 💎 My key learnings & challenges

The development was entirely remote and it is always a big experience for me and something that taught me just how flexible and resilient I can be.
<br>
<br>
My goal in this project was to identify best practices in order to have very productive days and successful remote working.
<br>
<br>
As a team, we quickly figure out how to start each day with a sprint stand-up and merging each other's codes in order to resolve any conflicts. We also had a shared worksheet to see and always remember the division of tasks.
<br>
<br>
On the day of the delivery (day 4), we were more organised and productive as we had already most features ready for deployment.
<br>
<br>
This only shows how much I could learn if I really throw myself into new challenges.
<br>
<br>
I started this project developing the `Job` data model and related features, here is a brief examples of my coding:

```jsx
class Job(models.Model):
    title = models.CharField(max_length=100)
    company = models.CharField(max_length=100)
    contract_type = models.CharField(max_length=100)
    salary = models.CharField(max_length=100)
    link = models.URLField(max_length=2000)
    description = models.TextField(max_length=2000)
    contact = models.CharField(max_length=150)
    requirements = models.ManyToManyField(Requirements)
    user = models.ForeignKey(User, on_delete=models.CASCADE)
    status = models.CharField(max_length=100, choices=STATUS_CHOICES, default='New')
    feedback = models.TextField(max_length=250, default='', blank=True)

    def get_absolute_url(self):
        return reverse('detail', kwargs = {'job_id': self.id})

    def __str__(self):
        return self.title
```
And `urls.py`:

```jsx
from . import views

urlpatterns = [
    path('', views.home, name='home'),
    path('about/', views.about, name='about'),
    path('jobs/', views.jobs_index, name='index'),
    path('jobs/<int:job_id>/', views.jobs_detail, name='detail'),
    path('jobs/create/', views.JobCreate.as_view(), name='jobs_create'),
    path('jobs/<int:pk>/update/', views.JobUpdate.as_view(), name='jobs_update'),
    path('jobs/<int:pk>/delete/', views.JobDelete.as_view(), name='jobs_delete'),
    path('jobs/<int:job_id>/add_requirement/', views.add_requirement, name='add_requirement'),
    path('jobs/<int:job_id>/edit_status/', views.edit_status_index, name='job_edit_status'),
]
```

I also integrated the many-to-many relationship between `Job` and `Requirement`. 

```jsx  
# M/M
    path('jobs/<int:job_id>/assoc_requirement/<int:requirement_id>/', views.assoc_requirement, name='assoc_requirement'),
    path('jobs/<int:job_id>/unassoc_requirement/<int:requirement_id>/', views.unassoc_requirement, name='unassoc_requirement'),
```
And creating the CRUD in `views.py`:

```jsx
class JobCreate(LoginRequiredMixin, CreateView):
    model = Job
    fields = ['title', 'company', 'contract_type', 'salary', 'link', 'description', 'contact']

    def form_valid(self, form):
        form.instance.user = self.request.user
        return super().form_valid(form)


class JobUpdate(LoginRequiredMixin, UpdateView):
    model = Job
    fields = ['title', 'company', 'contract_type', 'salary', 'link', 'description', 'contact']

    def form_valid(self, form):
        form.instance.user = self.request.user
        return super().form_valid(form)

# For the modal button on index
def edit_status_index(request, job_id):
    instance = get_object_or_404(Job, id=job_id)
    s_form = StatusForm(instance=instance) 
    if request.method == 'POST':
        s_form = StatusForm(request.POST, instance=instance)

        if s_form.is_valid():
            s_form.save(commit=True)
            # messages.success(request, f'Updated Successfully')

            return HttpResponse(s_form.as_table())
        else:
            print("Not updated, you can 'see details' and edit there")
    return HttpResponse(s_form.as_table())
    


class JobDelete(LoginRequiredMixin, DeleteView):
    model = Job
    success_url = '/jobs/'
```


***

### 🔎 Delivered Features:
* Authentication and authorization;
* Display messages for signup, signin and update profile;
* Add, edit and delete a job;
* Add, edit and delete a requirement
* Choose a status for the job directly on the index page;
* View all jobs on one page;
* Add or remove a requirement for a job directly on the job detail page;
* M/M: many jobs can have many requirements;
* User can view their profile information and update user profile as a pop up on the profile page;
* User can add a photo, CV link, cover letter link on their profile;
* User can also change their password while logged in;
* Dark mode option using local storage.

***

### 📍 Getting Started
* Sign up [here](https://jobtrackersei64.herokuapp.com/accounts/signup/).
* Your password must be 6 characters long, with at least an uppercase and one number, example: `Pass123`.
* Then, explore the app and enjoy the features!
![AddAJob](/img/add-a-job-page.jpg)
![IndexPage](/img/index-page.jpg)
![JobDetailPage](/img/job-detail-page.jpg)

***

### 💡 Nice to have future enhancements:
- Use API to upload a job automatically
- Use web scraping to find and pull jobs from job sites
- Add password reset by email
- Remove unsuccessful jobs from index page 
- Unsuccessful job status goes to a different page
- View all feedback from unsuccessful jobs in one place
- Change the colour of the emphasis line when filling out forms (using SASS)
- More styling.

***

### 🐞 Bugs

The `signup` page can still be accessed by logged in users, this should be redirected to the `job index page`.
Details on how to choose a password should be added in the `signup` page. The app only accepts ***6 characters long with one uppercase and one number***.

***

### 👋 Team members
* Yamily Benigni - [Linkedin](https://www.linkedin.com/in/yamilybenigni/)
* Ailish McLaughlin - [Linkedin](https://www.linkedin.com/in/ailish-mclaughlin/)
* Bedros Asdorian - [Linkedin](https://www.linkedin.com/in/bedros-asdorian-7ba548188/)

***

### 💜 Quote
*"Just one small positive thought in the morning can change your whole day."* - Dalai Lama

***

##### This app has been developed while on the General Assembly Software Engineering Immersive Programme.
