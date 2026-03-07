Created a repo github-actions-practice
then clone to local machine


### Hello Workflows

```
name: hello worksflow
on:
    push:
        branches: [main]
jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
    - name: checkout-code
      uses: actions/checkout@v4
    - name: print greeting
      run: echo ""Hello from GitHub Actions!"
```

<img width="1024" height="635" alt="hello workflows" src="https://github.com/user-attachments/assets/59b6b502-9c5c-4b96-8926-c06319a5d32a" />

### Print current date 
```
name: hello worksflow
on:
    push:
        branches: [main]
jobs:
  greet:
    runs-on: ubuntu-latest
    steps:
    - name: checkout-code
      uses: actions/checkout@v4
    - name: print greeting
      run: echo ""Hello from GitHub Actions!"
    - name: print current date and time
      run: date "+%y-%m-%d %H:%M:%S"
```
<img width="1015" height="640" alt="current_date_time" src="https://github.com/user-attachments/assets/8695e103-fb1b-4db5-890d-7bc786b52d2d" />
nd time
