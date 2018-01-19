# PHP Datetime Range

## Create date range

```php

      $dateTo = new \DateTimeImmutable();
      $dateFrom = $dateTo->modify('-30 days');
      $interval = new \DateInterval('P1D');
      
      $datePeriod = new \DatePeriod($dateFrom, $interval, $dateTo);
      
      $dateRange = new \DateTimeRange();
      $dateRange->setDates(iterator_to_array($datePeriod));
    
      while ($dateRange->next()) {
          $day = $dateRange->getDate();
          echo $day->format('j.n.');
      }
```
