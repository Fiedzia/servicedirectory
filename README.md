#Service directory for ws -  webservice command-line tool.

This repository contains service definitions for ws ().
Each service is described by json file(in utf-8), and placed within services/OWNER_OR_CATEGORY/NAME.json,
where OWNER_OR_CATEGORY is a directory, and NAME is service name.

An example of a service definition may look like this (taken from example/cowsay.json): 

    {
        "name": "cowsay",
        "summary": "Cowsay generates an ASCII picture of a cow saying something provided by the user",
        "description": "Cowsay\n\nGenerates an ASCII picture of a cow saying something provided by the user.\nBest example ever invented",
        "protocols": ["http/GET"],
        "uri": {"http/GET": "cowsay.linuxcoder.co.uk/cowsay/"},
        "author": "Maciej Dziardziel",
        "homepage": "http://cowsay.linuxcoder.co.uk/cowsay/"
    }


#Fields

All fields presented in this example are mandatory.
Their meaning is as follows:

name:

		service name

summary:

		one-line service description

description:

		longer description of the service, may contain multiple lines (using \n as line break)
		If its longer then few kilobytes, it probably deserves separate page for documentation.

protocols:

		List of supported protocols, which will be used in the order of appearance.
		Supported values are:
			http/GET: http, with parameters passed as GET
			http/POST: http, with parameters passed as POST
			(support for https/GET and https/POST will be added later)

uri:

		service uri, in the form DOMAIN_OR_IP[:PORT]/resource

author:

		service author or owner. Can be username, or company name

homepage:

		Service homepage. Place where users should go to get more informations about the service.
