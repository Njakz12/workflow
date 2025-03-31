# Creating an AWS ecoystem using terraform


[ Terraform Config ]
       │
       ▼
┌─────────────────────┐
│ 1. VPC Creation     │
│ (10.0.0.0/16)       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 2. Internet Gateway │
│ (Attached to VPC)   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 3. Public Subnet    │
│ (10.0.1.0/24)       │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 4. Route Table      │
│ (0.0.0.0/0 → IGW)   │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 5. Security Group   │
│ (Allow SSH inbound) │
└──────────┬──────────┘
           │
           ▼
┌─────────────────────┐
│ 6. EC2 Instance     │
│ (Public IP assigned)│
└─────────────────────┘
