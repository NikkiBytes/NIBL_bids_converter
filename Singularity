
Bootstrap: docker
From:nipy/heudiconv


%post

	# commands executed inside the container during bootstrap
	echo "Packages installing....."
    echo "update..."
	apt-get -y update
    echo "python..."
	apt-get -y install python autoconf automake libtool flex
   






%runscript 
	# commands to be executed when the containers runs
    docker run -u 0 --rm -it -v $PWD:/data nipy/heudiconv -d /data/{subject}/*/raw/SM*/*/*.dcm -s SugarMama -f /heuristics/convertall.py -c none -o /data/test/output/{subject}
