# Deleting a DynamoDB Table Backup<a name="Delete.Tutorial"></a>

This section describes how to use the Amazon DynamoDB console or AWS CLI to delete a DynamoDB table backup\. \(If you want to use the AWS CLI, you have to configure it first\. For more information, see [Accessing DynamoDB](AccessingDynamoDB.md)\.\)

**Topics**
+ [Deleting a Table Backup \(Console\)](#deletebackup_console)
+ [Deleting a Table Backup \(AWS CLI\)](#deletebackup_cli)

## Deleting a Table Backup \(Console\)<a name="deletebackup_console"></a>

The following procedure shows how to delete the `MusicCollectionBackup` that is created in the [Backing Up a DynamoDB Table](Backup.Tutorial.md) tutorial\.

1. Sign in to the AWS Management Console and open the DynamoDB console at [https://console\.aws\.amazon\.com/dynamodb/](https://console.aws.amazon.com/dynamodb/)\.

1. In the navigation pane on the left side of the console, choose **Backups**\.

1. In the list of backups, choose `MusicCollectionBackup`\.  
![\[Screenshot showing the MusicCollectionBackup with status as available\]](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/images/deleteBackup.png)

1. Choose **Delete backup**:  
![\[Screenshot of the backups list with delete backup button highlighted.\]](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/images/deleteBackupSelected.png)

   Choose **Delete** to delete the backup\.  
![\[Screenshot of the delete backup screen.\]](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/images/ConfirmDeleteBackup.png)

## Deleting a Table Backup \(AWS CLI\)<a name="deletebackup_cli"></a>

The following example deletes a backup for an existing table `MusicCollection` using the AWS CLI\.

```
aws dynamodb delete-backup \
--backup-arn arn:aws:dynamodb:us-east-1:123456789012:table/MusicCollection/backup/01489602797149-73d8d5bc
```