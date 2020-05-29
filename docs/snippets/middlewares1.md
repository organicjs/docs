module.exports = function(app) {
	
    var http = require('http');
    var path = require('path');
    var csrf = require('csrf');
    var logger = require('morgan');
    var session = require('express-session');
    var bodyParser = require('body-parser');
    var cookieParser = require('cookie-parser');
    var connectFlash = require('connect-flash');
    var errorHandler = require('errorhandler');
    
	/**
	 * Use body-parser.
	 */
	app.use(bodyParser.json());
	app.use(bodyParser.urlencoded({extended: true}));
	
	/**
	 * Use cookie-parser.
	 */
	app.use(cookieParser('weird-cookie-secret'));
	
	/**
	 * Use express-session.
	 */
	app.use(session({
		secret: 'i-stole-your-cat',
		cookie: {maxAge: 60000},
		resave: false,
		saveUninitialized: true
	}));
	
	/**
	 * Use connect-flash.
	 */
	app.use(connectFlash());
	
};	