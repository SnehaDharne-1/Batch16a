**git_assignment_HeroVired
Q1: CalculatorPlus Application**
**Objective**
Enhance the CalculatorPlus Python application by:
•	Adding a square root feature
•	Handling a critical bug
•	Following proper Git workflow practices
**Steps Performed**
**1.	Repository Setup**
o	Created private GitHub repository: git_assignment_HeroVired
o	Cloned repository locally
o	Added initial README.md
**2.	Development Branch Setup**
o	Created dev branch
o	Added base application code in CalculatorPlus.py with:
	Addition
	Subtraction
	Multiplication
	Division
**3.	Initial Release (v1.0)**
o	Merged dev branch into main
o	Tagged release: v1.0
**4.	Feature Development - Square Root**
o	Created feature branch: feature/sqrt
o	Implemented:
o	def square_root(self, x):
    return math.sqrt(x)
o	Uncommented and tested square root functionality
**5.	Bug Fix (Hotfix)**
o	Created branch: hotfix/divide-error-fix
o	Fixed divide function:
o	def divide(self, a, b):
o	    if b == 0:
o	        raise ValueError("Cannot divide by zero.")
    return a / b
**6.	Pull Request Workflow**
o	Created PR: hotfix/divide-error-fix → dev
o	Merged after review
o	Updated feature branch: git pull origin dev
o	Created PR: feature/sqrt → main
o	Requested code review and applied feedback
**7.	Final Integration**
o	Merged feature/sqrt into dev
o	Tested application in dev
o	Merged dev → main
**8.	Final Release (v2.0)**
o	Tagged release: v2.0
**9.	Collaboration**
o	Added classmate as collaborator
o	Participated in peer code review
________________________________________
**Q2: Git LFS (Large File Storage)
Objective**
Handle large binary files efficiently using Git LFS.
**Steps Performed**
**1.	LFS Setup**
o	Installed Git LFS: git lfs install
**2.	Created LFS Branch**
o	git checkout -b lfs
**3.	Configured Tracking**
o	git lfs track "*.zip"
**4.	Added Large File**
o	Added file: dummyfile01.zip (>200MB)
o	Committed and pushed to repository
**5.	Verification**
o	Cloned repository on another system
o	Installed Git LFS
o	Executed: git lfs pull
o	Verified file using: git lfs ls-files
**6.	Issue Faced & Resolution**
o	Issue: Switching branches due to .gitattributes
o	Resolution:
	git stash --include-untracked
	Observed delay during checkout due to large file download
	Used:
	GIT_LFS_SKIP_SMUDGE=1 git checkout lfs
git lfs pull
________________________________________
**Q3: Geometry Calculator (Git Stash)
Objective**
Implement multiple features using Git stash while switching branches.
**Steps Performed**
**1.	Base Branch Creation**
o	git checkout -b geometry-calculator
o	Created GeometryCalculator.py
o	Added base functions:
	Circle area
	Rectangle area
**2.	Circle Feature**
o	git checkout -b feature/circle-area
o	Implemented circle area logic
o	Stashed incomplete changes: git stash
**3.	Rectangle Feature**
o	git checkout -b feature/rectangle-area
o	Implemented rectangle logic
o	Stashed changes: git stash
**4.	Resume Circle Feature**
o	git checkout feature/circle-area
o	git stash pop
o	Completed implementation
o	Committed and pushed changes
**5.	Resume Rectangle Feature**
o	git checkout feature/rectangle-area
o	git stash pop
o	Completed implementation
o	Committed and pushed changes
**6.	Pull Requests**
o	Created PRs:
	feature/circle-area → dev
	feature/rectangle-area → dev
o	Merged after review
**7.	Final Merge**
o	git checkout dev
o	git pull dev
o	git checkout main
o	git merge dev
o	git push origin main

