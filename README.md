# php-datetimerange

## Create date range

      $dateTo = new \DateTimeImmutable();
      $dateFrom = $dateTo->modify('-30 days');
      $interval = new \DateInterval('P1D');
      $datePeriod = new \DatePeriod($dateFrom, $interval, $dateTo);
      $dateRange = new \DateTimeRange();
      $dateRange->setDates(array_reverse(iterator_to_array($datePeriod)));
    
      while ($dateRange->next()) {
          $day = $dateRange->getDate();
          echo $day->format('j.n.');
      }
