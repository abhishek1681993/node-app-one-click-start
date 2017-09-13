@echo off

NET SESSION >nul 2>&1
set SETUP_DIR=%CD%
IF %ERRORLEVEL% NEQ 0 (
	echo This setup needs admin permissions. Please run this file as admin.
	pause
	exit
)

mkdir ap
cd ap
echo clone git repo at location desktop
git clone https://gist.github.com/3864088.git
REM echo INSTALLING grunt-less grunt-copy grunt-clean grunt-compress ...
REM call npm install grunt-contrib-less grunt-contrib-copy grunt-contrib-clean grunt-contrib-compress
cd %SETUP_DIR%
echo DONE!
