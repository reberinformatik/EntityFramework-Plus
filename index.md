---
layout: post
---

<html lang="en">
	<head>
		<meta charset="utf-8">
		<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
		<meta http-equiv="x-ua-compatible" content="ie=edge">
		<meta name="msvalidate.01" content="89359D9C492A475C0061398008D105FB" />
		
		<!-- seo !-->
		<meta name="description" content="Improve Entity Framework performance and overcome limitations with MUST-HAVE features">
		<meta name="keywords" content="BulkSaveChanges | Bulk Insert, Update, Delete and Merge | Query Cache | Query Filter | Query Future | Query IncludeFilter | Audit">
		<title>Entity Framework Utilities | Bulk Operations | Batch Delete | Batch Update | Query Cache | Query Filter | Query Future | Query Include | Audit</title>
		
		<!-- icon/css !-->
		<link rel="icon" type="image/png" href="http://entityframework-plus.net/images/logo.png">
		<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.2/css/bootstrap.min.css" integrity="sha384-y3tfxAZXuh4HwSYylfB+J125MxIs6mR5FOHamPBG064zB+AFeWH94NdvaCBm8qnd" crossorigin="anonymous">
		<link rel="stylesheet" type="text/css" href="https://maxcdn.bootstrapcdn.com/font-awesome/4.4.0/css/font-awesome.min.css">
		<link rel="stylesheet" type="text/css" href="http://entityframework-plus.net/css/github2.css">
		<link rel="stylesheet" type="text/css" href="http://entityframework-plus.net/css/default.css">
	</head>
	
	<body>
  
		<!-- top-header !-->
		<div id="top-header">
			<div class="container">
				<div class="text-right">
					<a href="mailto:info@zzzprojects.com"><i class="fa fa-envelope"></i>&nbsp;&nbsp;info@zzzprojects.com</a>
					<a href="https://www.facebook.com/zzzprojects" target="_blank"><i class="fa fa-facebook"></i></a>
					<a href="https://twitter.com/zzzprojects" target="_blank"><i class="fa fa-twitter"></i></a>
					<a href="https://plus.google.com/+Zzzprojects_NetSQL" target="_blank"><i class="fa fa-google-plus"></i></a>
					<a href="http://zzzprojects.us9.list-manage.com/subscribe?u=cecbc4775cf67bf1ff82018af&id=4765ffa5f8" target="_blank" class="hidden-xs-down"><i class="fa fa-newspaper-o"></i></a>
				</div>
			</div>
		</div>
		
		<!-- header !-->
		<header>
			<div class="container">
				<div class="row">
					<div class="col-lg-6">
						<div class="card">
							<div class="card-block">
								<h3 class="card-title">EntityFramework Plus</h3>
								<hr class="m-y-md" />
								<h1>Improve Entity Framework performance and overcome limitations with MUST-HAVE features</h1>
								<hr class="m-y-md" />
								<div class="lead">
									<a href="https://github.com/zzzprojects/EntityFramework-Plus/wiki/Downloads" target="_blank" class="btn btn-success btn-lg btn-left" role="button" onclick="ga('send', 'event', { eventAction: 'download'});"><span><i class="fa fa-cloud-download fa-2x"></i>&nbsp;<span>Download</span></span></a>
									<a href="https://github.com/zzzprojects/EntityFramework-Plus" target="_blank" class="btn btn-primary btn-lg btn-right" role="button" onclick="ga('send', 'event', { eventAction: 'github'});"><span><i class="fa fa-github fa-2x"></i>&nbsp;<span>GitHub</span></span></a>		
								</div>
							</div>
						</div>
					</div>
					<div class="col-lg-6">
						<div class="card">
							<div class="card-block card-code">
{% highlight csharp %}
// Easy to use
context.BulkSaveChanges();

// Easy to customize
context.BulkSaveChanges(bulk => bulk.BatchSize = 100);

// Perform Bulk Operations
context.BulkDelete(customers);
context.BulkInsert(customers);
context.BulkUpdate(customers);

// Customize Primary Key
context.BulkMerge(customers, operation => {
   operation.ColumnPrimaryKeyExpression = 
        customer => customer.Code;
});
{% endhighlight %}	
							</div>
						</div>
					</div>
				</div>
			</div>
		</header>
		
<!-- featured !-->
		<div id="featured">
			<div class="container">
			
				<!-- Improve Performance !-->
				<h2>Improve SaveChanges Performance</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="featured-tagline">Use <span class="text-bold-red">scalable</span> bulk operations and always get the best <span class="text-bold-red">performance</span> available for your database provider.</p>
						<ul class="featured-list-sm">
							<li>SQL Server 2008+</li>
							<li>SQL Azure</li>
							<li>SQL Compact</li>
							<li>MySQL</li>
							<li>SQLite</li>
							<li>PostgreSQL <i>(Coming soon)</i></li>
							<li>Oracle <i>(Coming soon)</i></li>
						</ul>
						<p><i>Currently only available with <a href="http://entityframework-extensions.net/" target="_blank">Entity Framework Extensions</a> (Under migration to EF+)</i></p>
					</div>
					<div class="col-lg-7">
						<table class="table table-striped table-hover">
							<tr class="thead-inverse">
								<th>Operations</th>
								<th>1,000 Entities</th>
								<th>2,000 Entities</th>
								<th>5,000 Entities</th>
							</tr>
							<tr>
								<th>SaveChanges</th>
								<td>1,000 ms</td>
								<td>2,000 ms</td>
								<td>5,000 ms</td>
							</tr>
							<tr>
								<th>BulkSaveChanges</th>
								<td>90 ms</td>
								<td>150 ms</td>
								<td>350 ms</td>
							</tr>
							<tr>
								<th>BulkInsert</th>
								<td>6 ms</td>
								<td>10 ms</td>
								<td>15 ms</td>
							</tr>
							<tr>
								<th>BulkUpdate</th>
								<td>50 ms</td>
								<td>55 ms</td>
								<td>65 ms</td>
							</tr>
							<tr>
								<th>BulkDelete</th>
								<td>45 ms</td>
								<td>50 ms</td>
								<td>60 ms</td>
							</tr>
							<tr>
								<th>BulkMerge</th>
								<td>65 ms</td>
								<td>80 ms</td>
								<td>110 ms</td>
							</tr>
						</table>
						
						<p class="text-muted">* Benchmark for SQL Server</p>
					</div>
				</div>
			</div>
		</div>
		
		<!-- testimonials !-->
		<div id="testimonials">
			<div class="container">
				<h2>Amazing <span class="text-bold-red">performance</span>, outstanding <span class="text-bold-red">support</span>!</h2>
				<ul>
					<li>- "We were very, very pleased with the customer support. There was no question, problem or wish, that was not answered AND solved within days! We think that’s very unique!" Klemens Stelzmüller, <a href="http://www.beka-software.at/" target="_blank">Beka-software</a></li>
					<li>- "I’d definitely recommend it, as it is a great product with a great performance and reliability." Eric Rey, <a href="http://www.transturcarrental.com/" target="_blank">Transtur</a></li>
					<li>- "It’s great. It took me 5 minutes to implement it and makes my application 100x more responsive for certain database operations. Fill a big hole in Entity Framework." Dave Weisberg</li>
				</ul>
				<p><span class="text-bold-red">Share</span> your experience, we love to hear from you: <a href="mailto:info@zzzprojects.com">info@zzzprojects.com</a></p>
			</div>
		</div>
		
		<!-- features !-->
		<div id="feature">
			<div class="container">
				<!-- BulkSaveChanges !-->
				<a id="bulk-savechanges" href="#"></a>
				<h2>Bulk SaveChanges</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Improving your applications performance couldn’t have been made <span class="text-bold-red">easier</span>!</p>
						<ul>
							<li>Easy to use</li>
							<li>Easy to customize</li>
							<li>Easy to maintain</li>
						</ul>
						<p><i>Currently only available with <a href="http://entityframework-extensions.net/" target="_blank">Entity Framework Extensions</a> (Under migration to EF+)</i></p>
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// Easy to use
context.BulkSaveChanges();

// Easy to customize
context.BulkSaveChanges(operation => operation.BatchSize = 1000);
{% endhighlight %}
					</div>
				</div>

				<hr class="m-y-md" />
				
				<!-- Bulk Operations !-->
				<a id="bulk-operations" href="#"></a>
				<h2>Bulk Operations</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Use <span class="text-bold-red">flexible</span> features to overcome Entity Framework limitations</p>
						<ul>
							<li>Choose batch size</li>
							<li>Choose columns</li>
							<li>Choose primary key</li>
						</ul>
						<p><i>Currently only available with <a href="http://entityframework-extensions.net/" target="_blank">Entity Framework Extensions</a> (Under migration to EF+)</i></p>
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// Use all kind of bulk operations
context.BulkInsert(customers);
context.BulkUpdate(customers);
context.BulkDelete(customers);

// Customize your operation
context.BulkMerge(customers, operation => {
   operation.BatchSize = 1000;
   operation.ColumnPrimaryKeyExpression = customer => customer.Code;
});
{% endhighlight %}	
					</div>
				</div>

				<hr class="m-y-md" />
				
				<!-- Delete without loading entities !-->
				<a id="delete-without-loading-entities" href="#"></a>
				<h2>Delete without loading entities</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Delete rows from LINQ Query in a single database round trip without loading entities in the context</p>
						<ul>
							<li>Use Async methods to make your application responsive</li>
							<li>Use batch size to improve performance</li>
							<li>Use batch delay interval to reduce server load</li>
							<li>Use Intercept to customize DbCommand</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// DELETE all users inactive for 2 years
ctx.Users.Where(x => x.LastLoginDate < DateTime.Now.AddYears(-2))
         .Delete();

// DELETE using a BatchSize
ctx.Users.Where(x => x.LastLoginDate < DateTime.Now.AddYears(-2))
         .Delete(x => x.BatchSize = 1000);
{% endhighlight %}	
					</div>
				</div>
								
				<hr class="m-y-md" />
				
				<!-- Update without loading entities !-->
				<a id="update-without-loading-entities" href="#"></a>
				<h2>Update without loading entities</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Update rows from LINQ Query in a single database round trip without loading entities in the context</p>
						<ul>
							<li>Use Async methods to make your application responsive</li>
							<li>Use Intercept to customize DbCommand</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// UPDATE all users inactive for 2 years
ctx.Users.Where(x => x.LastLoginDate < DateTime.Now.AddYears(-2))
         .Update(x => new User() { IsSoftDeleted = 1 });
{% endhighlight %}	
					</div>
				</div>
								
				<hr class="m-y-md" />
				
				<!-- Auditing !-->
				<a id="auditing" href="#"></a>
				<h2>Auditing</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Improve <span class="text-bold-red">security</span> and know what, when and who did a changes in the context.</p>
						<ul>
							<li>AutoSave audit values in the database</li>
							<li>Keep track of SoftDelete entities</li>
							<li>Filter events you desire</li>
							<li>Include entity type you desire</li>
							<li>Format value in your specific format</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
var audit = new Audit();
audit.CreatedBy = "ZZZ Projects"; // Optional
ctx.SaveChanges(audit);

// Access to all auditing information
var entries = audit.Entries;
foreach(var entry in entries)
{
    foreach(var property in entry.Properties)
    {
    }
}
{% endhighlight %}	
					</div>
				</div>
								
				<hr class="m-y-md" />
				
				<!-- Second Level Cache !-->
				<a id="second-level-cache" href="#"></a>
				<h2>Second Level Cache</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Improve application <span class="text-bold-red">performance</span> and reduce sql server load by using a second level caching.</p>
						<ul>
							<li>Use Cache Tag to expire cache</li>
							<li>Use Cache Policy to control caching</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// The first call perform a database round trip
var countries1 = ctx.Countries.FromCache().ToList();

// Subsequent calls will take the value from the memory instead
var countries2 = ctx.Countries.FromCache().ToList();
{% endhighlight %}	
					</div>
				</div>
								
				<hr class="m-y-md" />
				
				<!-- Filtering !-->
				<a id="filtering" href="#"></a>
				<h2>Filtering</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Improve your context <span class="text-bold-red">extensibility</span> and create filters to query only what's really available.</p>
						<ul>
							<li>Create Multi-Tenancy application</li>
							<li>Exclude soft deleted record</li>
							<li>Filter record by security access</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
QueryFilterManager.Filter<Post>(q => q.Where(x => !x.IsSoftDeleted));

var ctx = new EntitiesContext();

// SELECT * FROM Post WHERE IsSoftDeleted = false
var list = ctx.Posts.ToList();
{% endhighlight %}	
					</div>
				</div>
								
				<hr class="m-y-md" />
				
				<!-- Future & FutureValue !-->
				<a id="future--futurevalue" href="#"></a>
				<h2>Future & FutureValue</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Delay queries execution and batch all queries in a single database round trip.</p>
						<ul>
							<li>Query Future</li>
							<li>Query Future Value</li>
							<li>Query Future Value Deferred</li>
							<li>Include entity type you desire</li>
							<li>Format value in your specific format</li>
						</ul>
						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// CREATE a pending list of future queries
var futureCountries = db.Countries.Where(x => x.IsActive).Future();
var futureStates = db.States.Where(x => x.IsActive).Future();

// TRIGGER all pending queries in one database round trip
// SELECT * FROM Country WHERE IsActive = true;
// SELECT * FROM State WHERE IsActive = true
var countries = futureCountries.ToList();

// futureStates is already resolved and contains the result
var states = futureStates.ToList();
{% endhighlight %}	
					</div>
				</div>
				
				<hr class="m-y-md" />
				
				<!-- Filter included related entities !-->
				<a id="filter-included-related-entities" href="#"></a>
				<h2>Filter included related entities</h2>
				<div class="row">
					<div class="col-lg-5">
						<p class="feature-tagline">Overcome Include method limitations by filtering included related entities.</p>
						<ul>
							<li>Filter child entities with IncludeFilter</li>
							<li>Improve performance with IncludeOptimized </li>
						</ul>						
					</div>
					<div class="col-lg-7">
{% highlight csharp %}
// LOAD orders and the first 10 active related entities.
var list = ctx.Orders.IncludeFilter(x => x.Items.Where(y => !y.IsSoftDeleted)
                                               .OrderBy(y => y.Date)
                                               .Take(10))
                     .ToList();
{% endhighlight %}	
					</div>
				</div>
				
			</div>
		</div>
		
		<!-- support !-->
		<a id="supports" href="#"></a>
		<div id="support">
			<div class="container">
				<h2>Test our outstanding Support</h2>
				<h3>We usually answer within the next business day, hour, or minutes!</h3>
				<div class="row">
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Contact Us</h4>
							</div>
							<a href="mailto:info@zzzprojects.com"><i class="fa fa-users fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Email our team for any type of questions. We love to hear from you!</p>
								<a href="mailto:info@zzzprojects.com">info@zzzprojects.com</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Documentation</h4>
							</div>
							<a href="https://github.com/zzzprojects/EntityFramework-Plus/wiki" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});"><i class="fa fa-folder-open fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Consult our complete documentation to help you getting started.</p>
								<a href="https://github.com/zzzprojects/EntityFramework-Plus/wiki" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});">Documentation</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Forum</h4>
							</div>
							<a href="https://github.com/zzzprojects/EntityFramework-Plus/issues" target="_blank" onclick="ga('send', 'event', { eventAction: 'forum'});"><i class="fa fa-weixin fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Visit the forum to propose new features or to discuss about the library.</p>
								<a href="https://github.com/zzzprojects/EntityFramework-Plus/issues" target="_blank" onclick="ga('send', 'event', { eventAction: 'forum'});">Forum</a>
							</div>
						</div>
					</div>
					<hr class="hidden-sm-up" />
					<div class="col-sm-6 col-lg-3">
						<div class="card">
							<div class="card-block">
								<h4 class="card-title">Open Source</h4>
							</div>
							<a href="https://github.com/zzzprojects/EntityFramework-Plus" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});"><i class="fa fa-github fa-5x"></i></a>
							<div class="card-block">
								<p class="card-text">Access the source of the library you're using to understand better its logic.</p>
								<a href="https://github.com/zzzprojects/EntityFramework-Plus" target="_blank" onclick="ga('send', 'event', { eventAction: 'github'});">GitHub</a>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		
		<!-- pricing !-->
		<a id="pro" href="#"></a>
		<div id="pricing">
			<div class="container">
				<div class="row">
					<div class="col-lg-6">
						<h2>Pricing</h2>
						<hr class="m-y-md" />
						<p>EntityFramework Plus (EF+) is the new major version of <a href="http://entityframework-extensions.net/" target="_blank">Entity Framework Extensions</a>. We are currently migrating all features one by one. Both license library are compatible.</p>
						<p class="pricing-tagline">Join thousands of projects already using entity framework extensions and make <span class="text-bold-red">YOUR</span> customers happy.</p>
						<ul>
							<li>Improve applications responsivity</li>
							<li>Minimize time your customers wait</li>
							<li>Maximize time your customers work</li>
						</ul>
						<p class="pricing-tagline">"Time Is Money" and your customers expect applications to respond as quickly as possible.</p>						
						<p class="pricing-tagline">"B.U.L.K" four letters that will dramatically changes your applications performance forever.</p>						
						<hr class="m-y-md" />
						<p>Every month, a <a href="https://github.com/zzzprojects/EntityFramework-Plus/wiki/Downloads" target="_blank" onclick="ga('send', 'event', { eventAction: 'download'});">FREE trial</a> of the PRO version is available to let you evaluate all its features without limitations.</p>						
					</div>
					<div class="col-lg-6">
						<table class="table table-hover table-bordered">
							<thead class="thead-inverse">
								<tr>
									<th></th>
									<th>FREE</th>
									<th>PRO</th>
								</tr>
							</thead>
							<tbody>
								<tr>
									<th>Bulk SaveChanges</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Insert</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Update</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Delete</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Bulk Merge</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Audit</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Batch Delete</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Batch Update</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Query Cache</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
							    <tr>
									<th>Query Deferred</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Query Filter</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Query Future</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Query IncludeFilter</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Query IncludeOptimized</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Commercial License</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Royalty-Free</th>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
								<tr>
									<th>Support & Upgrades (1 year)</th>
									<td><i class="fa fa-times fa-2x"></i></td>
									<td><i class="fa fa-check-square-o fa-2x"></i></td>
								</tr>
							</tbody>
						</table>
						
						<form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top" onsubmit="return purchase_validate()">
							<input type="hidden" name="cmd" value="_s-xclick">
							<input type="hidden" name="currency_code" value="USD">
							<fieldset class="form-group">
								<input type="hidden" name="on0" value="Seats">
								<select id="provider_type" name="hosted_button_id" class="form-control" onchange="selectProduct()">
									<option value="GS977QXB98R2C">SQL Server/ Azure Provider</option>
									<option value="5WVPWVNDGRHH6">SQL Compact Provider</option>
									<option value="55WDUT7ENJBKU">SQLite Provider</option>
									<option value="32JM43GUXW4ZW">MySQL Provider</option>
									<option value="TSCGQDC4YR2MQ">ALL Providers</option>
								</select> 
								<br />
								<select id="product_option" name="os0" class="form-control">
									<option id="seat1" value="1 seat">Bulk Operations $599 (1 seat)</option>
									<option id="seat2_4" value="2-4 seats" selected>Bulk Operations $799 (2-4 seats)</option>
									<option id="seat5_9" value="5-9 seats">Bulk Operations $999 (5-9 seats)</option>
									<option id="seat10_14" value="10-14 seats">Bulk Operations $1199 (10-14 seats)</option>
									<option id="seat15_19" value="15-19 seats">Bulk Operations $1399 (15-19 seats)</option>
								</select> 
							</fieldset>
							<div class="checkbox">
								<label>
									<input id="agree_agreement" type="checkbox">I have read and agree to the <a href="http://www.zzzprojects.com/license-agreement/" target="_blank">License Agreement</a>.
								</label>
							</div>
							<button type="submit" class="btn btn-success btn-lg"><span><i class="fa fa-shopping-cart"></i>&nbsp;<span>BUY NOW</span></span></button>
							<br />
							<div>* Contact us for invoice or payment method alternative.</div>
						</form>		
					</div>
				</div>
			</div>
			
			<!-- validation !-->
			<div id="error_validation" class="modal fade" tabindex="-1" role="dialog" aria-labelledby="modal_agreement" aria-hidden="true">
				<div class="modal-dialog" role="document">
					<div class="modal-content">
						<div class="modal-header">
							<h4 class="modal-title" id="modal_agreement">License Agreement</h4>
						</div>
						<div class="modal-body bg-danger">
							You must read and agree to the License Agreement.
						</div>
						<div class="modal-footer">
							<button type="button" class="btn btn-secondary" data-dismiss="modal">Close</button>
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- other product !-->
		<div id="product">
			<div class="container">
				<div class="row">
					<div class="col-lg-3">
						<h3>Entity Framework</h3>
						<ul>
							<li><a href="http://entityframework-extensions.net/" target="_blank">Entity Framework Extensions</a></li>
							<li><a href="http://entityframework-plus.net/" target="_blank">Entity Framework Plus (EF+)</a></li>
						</ul>
					</div>
					<div class="col-lg-3">
						<h3>Bulk Operations</h3>
						<ul>
							<li><a href="http://bulk-operations.net/" target="_blank">Bulk Operations</a></li>
						</ul>
					</div>
					<div class="col-lg-3">
						<h3>Expression Evaluator</h3>
						<ul>
							<li><a href="http://eval-sql.net/" target="_blank">Eval SQL.NET</a></li>
							<li><a href="http://eval-expression.net/" target="_blank">Eval Expression.NET</a></li>
						</ul>
					</div>
					<div class="col-lg-3">
						<h3>Others</h3>
						<ul>
							<li><a href="https://github.com/zzzprojects/Z.ExtensionMethods" target="_blank">Extension Methods</a></li>
							<li><a href="https://github.com/zzzprojects/LINQ-Async" target="_blank">LINQ Async</a></li>
						</ul>
					</div>
				</div>
			</div>		
		</div>
		
		<!-- footer !-->
		<footer>
			<div class="container text-center-md-down">
				<div class="row">
					<div class="col-lg-6">
						Copyright © <a href="http://www.zzzprojects.com/" target="_blank" class="text-bold">ZZZ Projects Inc.</a> 2014 - 2016
						<div class="hidden-lg-up"></div>
						All rights reserved
					</div>
					<hr class="hidden-lg-up" />
					<div class="col-lg-6 text-right-lg-up social">
						<a href="https://www.facebook.com/zzzprojects" target="_blank"><i class="fa fa-facebook"></i></a>
						<a href="https://twitter.com/zzzprojects" target="_blank"><i class="fa fa-twitter"></i></a>
						<a href="https://plus.google.com/+Zzzprojects_NetSQL" target="_blank"><i class="fa fa-google-plus"></i></a>
						<a href="http://zzzprojects.us9.list-manage.com/subscribe?u=cecbc4775cf67bf1ff82018af&id=4765ffa5f8" target="_blank"><i class="fa fa-newspaper-o"></i></a>
					</div>
				</div>
			</div>
		</footer>

	<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/jquery/2.1.4/jquery.min.js"></script>
	<script src="http://entityframework-plus.net/js/tether.min.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-alpha.2/js/bootstrap.min.js" integrity="sha384-vZ2WRJMwsjRMW/8U7i6PWi6AlO1L79snBrmgiDpgIWJ82z8eA5lenwvxbMV1PAh7" crossorigin="anonymous"></script>
	<script type="text/javascript">
	  (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
	  (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
	  m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
	  })(window,document,'script','//www.google-analytics.com/analytics.js','ga');

	  ga('create', 'UA-55584370-6', 'auto');
	  ga('send', 'pageview');
	  
	  function purchase_validate() {
		if($("#agree_agreement").prop('checked')) {
			return true;
		}
		
		$("#error_validation").modal('show')
		return false;
	  }
	  
	  function selectProduct() {
		if($("#provider_type").val() == "TSCGQDC4YR2MQ") {
			$("#seat1").html("Entity Framework Extensions $799 (1 seat)");
			$("#seat2_4").html("Entity Framework Extensions $999 (2-4 seats)");
			$("#seat5_9").html("Entity Framework Extensions $1199 (5-9 seats)");
			$("#seat10_14").html("Entity Framework Extensions $1399 (10-14 seats)");
			$("#seat15_19").html("Entity Framework Extensions $1599 (15-19 seats)");
		}
		else {
			$("#seat1").html("Entity Framework Extensions $599 (1 seat)");
			$("#seat2_4").html("Entity Framework Extensions $799 (2-4 seats)");
			$("#seat5_9").html("Entity Framework Extensions $999 (5-9 seats)");
			$("#seat10_14").html("Entity Framework Extensions $1199 (10-14 seats)");
			$("#seat15_19").html("Entity Framework Extensions $1399 (15-19 seats)");
		}
	  }
	  
	  selectProduct();
	</script>
	</body>
</html>