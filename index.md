<html>

<head>
<meta http-equiv=Content-Type content="text/html; charset=utf-8">
</head>

<body>

<div>
<h2>How to get started with Git and GitHub?</h2>
<h4>
  1. brew install git    <i>#install git</i><br />
  2. brew install gh     <i>#install github</i><br />
  3. gh auth login       <i>#authenticate</i>
</h4>

<p>
  ? What account do you want to log into? GitHub.com<br />
  ? What is your preferred protocol for Git operations? HTTPS<br />
  ? Authenticate Git with your GitHub credentials? Yes<br />
  ? How would you like to authenticate GitHub CLI? Login with a web browser<br />
</p>

<h4>4. gh repo create      <i>#create repository</i></h4>
<p>
	? What would you like to do? Create a new repository on GitHub from scratch<br />
	? Repository name fundamental_analysis_&_valuation<br />
	? Description This code calculates the Entry, Exit price for an investible<br />
	? Visibility Private<br />
	? Would you like to add a .gitignore? Yes<br />
	? Choose a .gitignore template Python<br />
	? Would you like to add a license? No<br />
	? This will create "fundamental_analysis_-_valuation" as a private repository on GitHub. Continue? Yes<br />
	✓ Created repository premkrishnan/fundamental_analysis_-_valuation on GitHub<br />
	? Clone the new repository locally? Yes<br />
</p>

<h4>
5. git status			<i>#check status to know which files are available to 'add'</i><br />
6. git add .			<i>#add all files to commit</i><br />
7. git status			<i>#check status to know which files are available to 'commit'</i><br />
8. git commit -m "Comments"	<i>#commit changes</i><br />
</h4>
<h4>
9.0. git push origin main	<i>#push to the main or other branches</i>
</h4>
<p><i>
Error:<br />
	! [rejected]        main -> main (fetch first)<br />
	error: failed to push some refs to 'https://github.com/premkrishnan/fundamental_analysis_-_valuation.git'<br />
	hint: ...........................................<br />
	hint: (e.g., 'git pull ...') before pushing again.<br />
	hint: See the 'Note about fast-forwards' in 'git push --help' for details.<br /></i>
Solution:<br />
	The error was caused when tried to update the 'main' branch. It might be because there are changes happened at the main brach elsewhere. So, before commiting the lcoal changes, we must fetch, pull the changes and update/merge the local copy. <br />
	<b>9.1. Fetch:	git fetch origin</b><br />
	<b>9.2. Pull:	git pull origin main</b><br />
	<i>Warning:<br />
		hint: You have divergent branches and need to specify how to reconcile them.<br />
		hint: You can do so by running one of the following commands sometime before<br />
		hint: your next pull:<br />
		Merge branch 'main' of https://github.com/premkrishnan/fundamental_analysis_-_valuation<br />
		hint:   git config pull.rebase false  <i>#merge</i><br />
		hint:   git config pull.rebase true   <i>#rebase</i><br />
		hint:   git config pull.ff only       <i>#fast-forward only</i><br />
		hint: You can replace "git config" with "git config --global" to set a default<br />
		hint: ..........<br />
		fatal: Need to specify how to reconcile divergent branches.<br /></i>
	<b>9.3. Merge:	git config pull.rebase false</b><br />
			<b>9.4. git pull origin main</b><br />
</p>

<h3>Try 'push' again</h3>
<h4>
9.5. git push origin main	<i>#push to the main or other branches</i>
</h4>

</div>

</body>

</html>
