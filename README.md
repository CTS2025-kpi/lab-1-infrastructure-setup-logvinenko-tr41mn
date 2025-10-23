# Lab 1: AWS Infrastructure Setup

## 1. AWS Account Registration
Initial AWS account creation and setup process.

![AWS Registration](screenshots/1-register.png)

## 2. Account and User Setup


Створено юзера в Identity Center

![User Creation](screenshots/2-user.png)

Створено групу, додано туди користувача

![Identity Center Group](screenshots/2-ic-group.png)

Створено permission set.

![Identity Center Admin Permissions](screenshots/2-ic-permission-admin.png)


Додано permission set до групи

![Identity Center Account View](screenshots/2-ic-account-view.png)



## 3. AWS Organizations Configuration

Створено Organization Unit

![Organization View with Identity Center](screenshots/3-org-view-1-ic.png)

Додано другий акаунт в організацію

![Second Account - View 1](screenshots/3-org-view-2nd-acc-1.png)

Огляд організації з другого акаунту

![Second Account - View 2](screenshots/3-org-view-2nd-acc-2.png)

## 4. IAM ReadOnly Role and Policy

Створено IAM user-а.

![IAM User](screenshots/4-iam-user.png)

Створено ReadOnly Policy

![ReadOnly Policy](screenshots/4-readonly-policy.png)
[ReadOnly Policy JSON](files/ReadOnly.json)

Створено роль з ReadOnly policy:

![ReadOnly Role](screenshots/4-readonly-role.png)

та дозволено її використання зі створеного IAMuser:

[Trust Policy for ReadOnly Role](files/TrustPolicyReadOnlyRole.json)

Вхід через IAM user-a та переключення на роль:

![ReadOnly Sign In](screenshots/4-readonly-sign-in.png)

Також CloudFormation Template для ролі і політики (експорт з IaC-generator):

![CloudFormation Template Generator](screenshots/5-cf-templ-gen.png)
[CloudFormation Template for IAM](files/CFTempl.yaml)


## 6. VPC Infrastructure

VPC ресурси:
![VPC Overview](screenshots/6-vpc-view.png)


Публічна підмережа:

![Public Subnet](screenshots/6-vpc-subnet-public.png)

Приватна підмережа:

![Private Subnet](screenshots/6-vpc-subnet-private.png)

Публічна route talbe:

![Public Route Table](screenshots/6-vpc-route-table-public.png)

Приватна route talbe:

![Private Route Table](screenshots/6-vpc-route-table-private.png)

Internet Gateway для публічної таблиці:

![Public Gateway](screenshots/6-vpc-public-gateway.png)

**Configuration File:**


## 7. VPC CloudFormation Stack

Створено CloudFormation Template для ресурсів VPC:
[CloudFormation Template for VPC](files/CFTemplVPC.yaml)

та на його основі створено stack:

![VPC CloudFormation Stack](screenshots/7-vpc-cf-stack.png)

## 8. Cost Calculation

Підрахунок коштів для лаби 2 (EC2 2x)

![Cost Analysis](screenshots/8-cost-calculation.png)
