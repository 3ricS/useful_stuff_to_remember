# .screenrc
Diese Datei sollte im Home-Verzeichnis als `.screenrc` abgelegt werden:

    startup_message off
    altscreen               on
    hardstatus              string "%t%? [%h]%?"
    caption always "%{WB}%H %{kG}%?%-Lw%?%{bw}%n*%f%t%?(%u)%?%{kG}%?%+Lw%? %88=%{YR}%m-%d %94=%{RY}%c%="

    # Enable mouse scrolling and scroll bar history scrolling
    # termcapinfo xterm* ti@:te@

