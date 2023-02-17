# Cloud Computing Assignment 2a

### PES1UG20CS084

### Aryansh Bhargavan

---

**Task 1**

>Screenshot of the running Docker Container after installing Jenkins
>
>![1](img/1.png)

**Task 2**

> Picture showing the console output after the build is successful
>
> ![2](img/2.png)
>
> Picture showing the Stable state of the task in Build History of Jenkins
>
> ![3](img/3.png)

**Task 3**

> Console output of second job
>
> ![4](img/4.png)
>
> Status page of first job
>
> ![5](img/5.png)
>
> Build History of Jenkins
>
> ![6](img/6.png)
>
> Jenkins Dashboard
>
> ![7](img/7.png)

**Task 4**

> Webhook added to your GitHub repository
>
> ![8](img/8.png)
>
> Console Output of second job displaying the change made in hello.cpp file
>
> ![9](img/9.png)

**Task 5**

> Code/script written to create basic pipeline using GitHub repository
>
> ```Jenkinsfile
> pipeline{
>     agent any
>     stages{
>         stage ('Build'){
>             steps{
>                 sh 'make'
>                 echo 'build stage successful'
>                 build job: 'PES1UG20CS084-1'
>             }
>         }
>         stage ('Test'){
>             steps{
>                 sh './hello_exec'
>                 echo 'test stage successful'
>             }
>         }
>         stage ('Deploy'){
>             steps{
>                 echo 'Deployment successful'
>             }
>         }
>     }
>     post{
>         failure{
>             echo 'Pipeline failed'
>         }
>     }
> }
> ```
>
> Output of working created pipeline, the screenshot should include 
>
> ​	● Stage view / Execution status of pipeline with all stages succeeded
>
> ​    ● Verify Declarative: Post Actions stage succeed for handling failures. 
>
> ![11](img/11.png)
>
> Console Output of the Pipeline
>
> ![10](img/10.png)
>
> Link to the created GitHub repository
>
> <a href="https://github.com/aryanshb/PES1UG20CS084_Jenkins">aryanshb/PES1UG20CS084_Jenkins</a>
>
> ---



