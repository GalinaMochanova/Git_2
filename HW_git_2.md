# Git branches


1. На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bug Reports
- SQL
- Charles
- Mobile testing
```
git branch Postman
git branch jmeter
git branch checklists
git branch bug_reports
git branch sql
git branch charles
git branch mobile_testing
```

2. Запушить все ветки на внешний репозиторий: 
```
git push --all
```
3. В ветке Bag Reports сделать текстовый документ со структурой баг репорта:
```
 git checkout bug_reports
 touch bug_report.txt
 vim bug_report.txt
 
 i
 
 Bug report structure

1. Summary
2. Description
3. Steps to reproduce
4. Enviroment
5. Reproducibility
6. Severity
7. Priority
~
esc
:wq
```
4. Запушить структуру багрепорта на внешний репозиторий:

```
git add bug_report.txt
git commit -m "add file bug_report.txt"
git push --set-upstream origin bug_reports
```
5. Вмержить ветку Bug Reports в Main:

```
git checkout main
git merge bug_reports
```
6. Запушить main на внешний репозиторий
```
git push -u origin main
```
7. В ветке CheckLists набросать структуру чек листа:
```
git checkout checklists
touch checklist_structure.txt
vim checklist_structure.txt

i

*Test Readiness Review*        *Status*
*************************************
All the Requirements finalized *Done
Test Plan created and reviewed *Done
Test Cases preparation done    *Done
Test Case review and sign off  *Done
Test Data availability         *Done
Smoke Testing                  *Done

esc 
:wq
```
8. Запушить структуру на внешний репозиторий:
```
git add .
git commit -m "add file checklist_structure.txt"
git push --set-upstream origin checklists
```
9. На внешнем репозитории сделать Pull Request ветки CheckLists в main
```
Compare & Pull request -> Create pull request
	->Merge pull request -> Congfirm Merge
  ```
10. Синхронизировать Внешнюю и Локальную ветки Main:
```
git pull 
```
