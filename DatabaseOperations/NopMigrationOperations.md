# Data Table Attributes
This article covers All about Nop Datatables
```csharp
using FluentMigrator;

namespace Nop.Data.Migrations
{
    [Migration(20230101)] // The number is a unique identifier for the migration, usually a timestamp
    public class MyCustomMigration : Migration
    {
        public override void Up()
        {
            // Create a new table
            Create.Table("MyNewTable")
                .WithColumn("Id").AsInt32().PrimaryKey().Identity()
                .WithColumn("Name").AsString();

	        Rename.Column("OldColumnName").OnTable("MyTable").To("NewColumnName");

            // Add a new column to an existing table
            Alter.Table("ExistingTable")
                .AddColumn("NewColumn").AsString().Nullable();

            // Insert data into a table
            Insert.IntoTable("MyNewTable")
                .Row(new { Name = "Sample Data" });

            // Rename a table
            Rename.Table("OldTableName").To("NewTableName");

            // Change a column type
            Alter.Table("MyTable")
                .AlterColumn("MyColumn").AsInt64();

            // Add a foreign key
            Create.ForeignKey("FK_MyTable_OtherTable")
                .FromTable("MyTable").ForeignColumn("ForeignKeyColumn")
                .ToTable("OtherTable").PrimaryColumn("Id");

            // ... other database schema changes
        }

        public override void Down()
        {
            // Reverse the changes made in the Up() method
        }
    }
}

```

