## IAM Policy Breakdown

### Policy

```json
{
  "Id": "Policy1690260299236",
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Stmt1690260012453",
      "Action": "s3:*",
      "Effect": "Deny",
      "Resource": "arn:aws:s3:::jam-challenge-patientdata-us-east-1-569419362345",
      "Principal": {
        "AWS": [
          "arn:aws:iam::569419362345:user/USER-A"
        ]
      }
    },
    {
      "Sid": "Stmt1690260048278",
      "Action": "s3:*",
      "Effect": "Allow",
      "Resource": "arn:aws:s3:::jam-challenge-patientdata-us-east-1-569419362345",
      "Principal": {
        "AWS": [
          "arn:aws:iam::569419362345:user/USER-B"
        ]
      }
    }
  ]
}
```

### Breakdown

- `Id`: This is the unique identifier for the policy. It's optional and usually auto-generated if not provided.

- `Version`: This defines the version of the policy language. As of now, the 2012-10-17 version is the latest and most common.

- `Statement`: This is an array of individual statements (policies). Each statement is a standalone policy within the overall IAM policy.

Each `Statement` has the following elements:

- `Sid`: This stands for "statement identifier". It's an optional identifier for a policy statement.

- `Action`: Defines what actions are allowed or denied by the policy. In this case, "s3:*" means the policy applies to all S3 actions.

- `Effect`: Defines the effect of the policy. It can be either "Allow" or "Deny". Here, the policy explicitly denies USER-A and allows USER-B.

- `Resource`: Specifies the object or objects to which the action applies. This policy applies to the specified S3 bucket.

- `Principal`: Specifies who (users, groups, services, etc.) the policy applies to. This policy applies to USER-A in the first statement and USER-B in the second.

This policy essentially says: "Deny USER-A all actions on the specified S3 bucket, and Allow USER-B all actions on the same bucket."