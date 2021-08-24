# Customers Table

```d
CREATE TABLE `Customers` (
  `CustomerID` varchar(50) NOT NULL,
  `FirstName` varchar(45) NOT NULL,
  `LastName` varchar(45) DEFAULT NULL,
  `Email` varchar(45) DEFAULT NULL,
  `Phone` varchar(45) DEFAULT NULL,
  `Address` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`CustomerID`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

# Orders Table

```d
CREATE TABLE `Orders` (
  `OrderID` varchar(50) NOT NULL,
  `CustomerID` varchar(45) NOT NULL,
  `OrderDate` varchar(45) DEFAULT NULL,
  `CardNo` varchar(45) DEFAULT NULL,
  `OrderStatus` varchar(45) DEFAULT NULL,
  `ShippingAddress` varchar(45) DEFAULT NULL,
  `OrderDetails` varchar(45) DEFAULT NULL,
  `OrderItems` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`OrderID`),
  KEY `customerid_idx1` (`CustomerID`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

# Accounts Table
```d
CREATE TABLE `Accounts` (
  `AccountsID` varchar(50) NOT NULL,
  `CustomerID` varchar(45) NOT NULL,
  `EmployeesCount` int(11) DEFAULT NULL,
  `Industry` varchar(45) DEFAULT NULL,
  `Type` varchar(45) DEFAULT NULL,
  `Description` varchar(45) DEFAULT NULL,
  `Website` varchar(45) DEFAULT NULL,
  `Address` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`AccountsID`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```

# Users Table
```d
CREATE TABLE `Users` (
  `UserID` varchar(50) NOT NULL,
  `Email` varchar(45) DEFAULT NULL,
  `LastLogin` varchar(45) DEFAULT NULL,
  `Phone` varchar(45) DEFAULT NULL,
  `ProfilePicture` varchar(45) DEFAULT NULL,
  `AccountType` varchar(45) DEFAULT NULL,
  `PaymentType` varchar(45) DEFAULT NULL,
  PRIMARY KEY (`UserID`)
) ENGINE=InnoDB DEFAULT CHARSET=latin1;
```