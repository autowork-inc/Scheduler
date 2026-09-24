## Overview
This is a desktop application I built using React and Electron to manage local media libraries and schedule content across multiple accounts. I had a large volume of media files that needed to be distributed to specific accounts on a schedule, so I made this UI to automate the planning and exporting process. Due to the specific nature of the Python processing scripts it interacts with, the full source code is private, but here is a quick overview of the architecture

## Key Features
The frontend is a React SPA styled with Tailwind CSS, communicating with an Electron backend via IPC. The main dashboard features an account manager and a calendar panel where you can generate weekly or monthly content plans. To prevent mistakes, I added a rules engine where you can map specific local folders to account statuses. The most complex part of the app is the export pipeline. Once the schedule is set, the app triggers a process that collects all planned media and hands it off to a separate Python script. This script processes the files and prepares the final payload for ADB to push the files directly to connected physical phones

## Tech Stack
**React, Tailwind CSS, React Router, Electron, Python 3.11**
