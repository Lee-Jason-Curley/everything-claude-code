# Copy agents
New-Item -ItemType Directory -Path "C:\Users\clari\.claude\agents" -Force
Copy-Item -Path "./agents/*.md" -Destination "C:\Users\clari\.claude\agents" -Force

# Copy rules
New-Item -ItemType Directory -Path "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/common"      "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/csharp"  "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/python"      "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/rust"      "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/typescript"         "C:\Users\clari\.claude\rules" -Force
Copy-Item -Recurse "./rules/web"         "C:\Users\clari\.claude\rules" -Force

# Copy skills
Copy-Item -Recurse "./skills/search-first" "C:\Users\clari\.claude\skills" -Force
Copy-Item -Recurse "./.agents/skills/*" "C:\Users\clari\.claude\skills" -Force