# PHP Datetime Range

## Create date range

```php

      $dateTo = new \DateTimeImmutable();
      $dateFrom = $dateTo->modify('-30 days');
      $dateRange = new DateTimeRange($dateFrom, $dateTo);
    
      while ($dateRange->next()) {
          $day = $dateRange->getDate();
          echo $day->format('d.m.Y');
      }
      
      // RESULT CAN LOOKS LIKE THAT
      01.01.2000
      02.01.2000
      03.01.2000
      ...
```
