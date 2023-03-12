if [ -z "$1" ] && [ -z "$2" ]; then
  #if no parameters given assume its a file sync
   read -p "Are you sure you want to a total sync (PULL) from EFS to disk? (CAUTION: DESTROYS FILES ON DISK IF NOT ALREADY IN EFS) (y/n) " yn
   if [ "$yn" = "y" ]; then
    echo "Big sync from EFS to disk underway..."
    sudo /home/dave/files-pull.sh
    sudo /home/dave/themes-pull.sh
    sudo /home/dave/plugins-pull.sh
   fi
else
  if [ "$1" = "plugins" ]; then
    if [ "$2" = "push" ]; then
      if [ -z "$3" ]; then
        read -p "Are you sure you want to push plugins to EFS? (y/n) " yn
        if [ "$yn" = "y" ]; then
          echo "Pushing new plugins to EFS"
          sudo /home/dave/plugins-push.sh
        fi
      elif [ "$3" = "-y" ]; then
        echo "Pushing new plugins from disk to EFS"
        sudo /home/dave/plugins-push.sh
      fi
    elif [ "$2" = "pull" ]; then
      if [ -z "$3" ]; then
        read -p "Are you sure you want to pull staged plugins from EFS to disk? (y/n) " yn
        if [ "$yn" = "y" ]; then
          echo "Pulling existing plugins from EFS to Disk"
          sudo /home/dave/plugins-pull.sh
        fi
      elif [ "$3" = "-y" ]; then
        echo "Pulling existing plugins to Disk"
        sudo /home/dave/plugins-pull.sh
      fi
    fi
  elif [ "$1" = "themes" ]; then
    if [ "$2" = "push" ]; then
      if [ -z "$3" ]; then
        read -p "Are you sure you want to push theme updates to EFS? (y/n) " yn
        if [ "$yn" = "y" ]; then
          echo "Pushing theme updates to EFS"
          sudo /home/dave/themes-push.sh
        fi
      elif [ "$3" = "-y" ]; then
        echo "Pushing theme updates to EFS"
        sudo /home/dave/themes-push.sh
      fi
    elif [ "$2" = "pull" ]; then
      if [ -z "$3" ]; then
        read -p "Are you sure you want to pull theme updates from EFS to disk? (y/n) " yn
        if [ "$yn" = "y" ]; then
          echo "Pulling themes updates from EFS to disk"
          sudo /home/dave/themes-pull.sh
        fi
      elif [ "$3" = "-y" ]; then
        echo "Pulling theme updates from EFS to disk"
        sudo /home/dave/themes-pull.sh
      fi
    fi
  elif [ "$1" = "files" ]; then
      if [ "$2" = "push" ]; then
        if [ -z "$3" ]; then
          read -p "Are you sure you want to push file updates to EFS? (y/n) " yn
          if [ "$yn" = "y" ]; then
            echo "Pushing file updates to EFS"
            sudo /home/dave/files-push.sh
          fi
        elif [ "$3" = "-y" ]; then
          echo "Pushing file updates to EFS"
          sudo /home/dave/files-push.sh
        fi
      elif [ "$2" = "pull" ]; then
        if [ -z "$3" ]; then
          read -p "Are you sure you want to pull file updates from EFS to disk? (y/n) " yn
          if [ "$yn" = "y" ]; then
            echo "Pulling file updates from EFS to disk"
            sudo /home/dave/files-pull.sh
          fi
        elif [ "$3" = "-y" ]; then
          echo "Pulling file updates from EFS to disk"
          sudo /home/dave/files-pull.sh
        fi
      fi
   fi
fi
