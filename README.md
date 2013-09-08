examples
========

Code Examples


POPULATING LISTS USING CONTENT FROM A DATABASE





            <?php
            $con = mysql_connect("localhost","blah","blah");
            if (!$con)
              {
              die('Could not connect: ' . mysql_error());
              }

            mysql_select_db("bohemiaw_sig", $con);

            $result = mysql_query("SELECT * FROM sig");

            while($row = mysql_fetch_array($result))
              {
              echo "<li style='background:url(images/" . $row['imgLoc'] . ") no-repeat;'></li>";

              }

            mysql_close($con);
            ?> 

            <?php
            $con = mysql_connect("localhost","blah","blah");
            if (!$con)
              {
              die('Could not connect: ' . mysql_error());
              }

            mysql_select_db("bohemiaw_news", $con);

            $result = mysql_query("SELECT * FROM news");

            while($row = mysql_fetch_array($result))
              {
              echo "<li>";
                echo "<p>";
                  echo"<span class='dater2'>" . $row['dater'] . "</span>";
                  echo $row['newsInputs'];
                echo "</p>";
              echo "</li>";

              }

            mysql_close($con);
            ?> 
