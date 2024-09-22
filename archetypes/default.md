---
title: "{{ replace .File.ContentBaseName "-" " " | title }}"
date: {{ .Date | time.Format ":date_full"}}
time: {{ .Date | time.Format ":time_full"}}
description: "About {{ replace .File.ContentBaseName "-" " " | title }}"
tags: ["Linux", "Git", "JAVA", "Spring Boot", "Testing", "Database", "CI/CD"]
draft: true
---