@Library('ot-jenkinJava-pipeline@master')

def codeUtils = new org.opstree.java.javaCodePipeline()

node{
  codeUtils.call(
git_url                = https://github.com/veduboy/spring3hibernate.git
git_branch             = master
java_version           = java8
project_name           = spring3hibernate
project_dir            = opstree/webapp
code_build             = true
commit_validation      = true
unit_test              = true
junit_report_path      = target/surefire-reports/*.xml
code_coverage          = true
cobertura_report_path  = target/site/cobertura/coverage.xml
coverage_percentage    = 80
pmd_scan               = true
pmd_report_path        = /target/pmd.xml
cpd_report_path        = /target/cpd.xml
code_quality           = true
checkstyle_report_path = target/checkstyle-result.xml
code_bugscan           = true
findbugs_report_path   = target/findbugs/findbugsXml.xml
sonar_scan             = true
sonar_url              = http://opstree.sonar.com
sonar_user             = admin
sonar_password         = adminpass
owasp_report_path      = ["opstree"]
snyk_scan              = false
snyk_package           = synk@latest
snyk_token_name        = opstree-api-token
cred_scan              = true
publish_s3             = false
s3_profile_name        = test
upload_path            = opstree/build/prod/
upload_region          = us-east-1
source_file            = *.war
recipients             = vedansh.pachori@opstree.com
notification_method    = slack


	)
}

                  
