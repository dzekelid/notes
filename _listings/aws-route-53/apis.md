---
name: AWS Route 53
x-slug: aws-route-53
description: Amazon Route 53 is a highly available and scalable cloud Domain Name
  System (DNS) web service. It is designed to give developers and businesses an extremely
  reliable and cost effective way to route end users to Internet applications by translating
  names like www.example.com into the numeric IP addresses like 192.0.2.1 that computers
  use to connect to each other. Amazon Route 53 is fully compliant with IPv6 as well.Amazon
  Route 53 effectively connects user requests to infrastructure running in AWS &ndash;
  such as Amazon EC2 instances, Elastic Load Balancing load balancers, or Amazon S3
  buckets &ndash; and can also be used to route users to infrastructure outside of
  AWS. You can use Amazon Route 53 to configure DNS health checks to route traffic
  to healthy endpoints or to independently monitor the health of your application
  and its endpoints. Amazon Route 53 Traffic Flow makes it easy for you to manage
  traffic globally through a variety of routing types, including Latency Based Routing,
  Geo DNS, and Weighted Round Robin&mdash;all of which can be combined with DNS Failover
  in order to enable a variety of low-latency, fault-tolerant architectures. Using
  Amazon Route 53 Traffic Flow&rsquo;s simple visual editor, you can easily manage
  how your end-users are routed to your application&rsquo;s endpoints&mdash;whether
  in a single AWS region or distributed around the globe. Amazon Route 53 also offers
  Domain Name Registration &ndash; you can purchase and manage domain names such as
  example.com and Amazon Route 53 will automatically configure DNS settings for your
  domains.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Notes
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/apis.md
specificationVersion: "0.14"
apis:
- name: AWS Route 53 API - Create Reusable Delegation Set
  x-api-slug: 20130401delegationset-post
  description: Creates a delegation set (a group of four name servers) that can be
    reused by multiplehosted zones. If a hosted zoned ID is specified, CreateReusableDelegationSetmarks
    the delegation set associated with that zone as reusableSend a POST request to
    the /2013-04-01/delegationset resource. The request body must include a document
    with a CreateReusableDelegationSetRequest element.NoteA reusable delegation set
    can't be associated with a private hosted zone/For more information, including
    a procedure on how to create and configure a reusabledelegation set (also known
    as white label name servers), see Configuring White Label NameServers.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401delegationset-post-openapi.md
- name: AWS Route 53 API - List Reusable Delegation Sets
  x-api-slug: 20130401delegationsetmarkermarkerampmaxitemsmaxitems-get
  description: To retrieve a list of your reusable delegation sets, send a GET request
    tothe /2013-04-01/delegationset resource. The response to this request includes
    aDelegationSets element with zero, one, or multiple DelegationSetchild elements.
    By default, the list of delegation sets is displayed on a single page. You cancontrol
    the length of the page that is displayed by using the MaxItems parameter.You can
    use the Marker parameter to control the delegation set that the listbegins with.
    Note Amazon Route 53 returns a maximum of 100 items. If you set MaxItems to a
    value greater than100, Amazon Route 53 returns only the first 100.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401delegationsetmarkermarkerampmaxitemsmaxitems-get-openapi.md
- name: AWS Route 53 API - Create Health Check
  x-api-slug: 20130401healthcheck-post
  description: Creates a new health check.To create a new health check, send a POST
    request to the/2013-04-01/healthcheck resource. The request body must include
    a documentwith a CreateHealthCheckRequest element. The response returns theCreateHealthCheckResponse
    element, containing the health check ID specifiedwhen adding health check to a
    resource record set. For information about adding health checksto resource record
    sets, see ResourceRecordSet:HealthCheckId in ChangeResourceRecordSets. If you
    are registering EC2 instances with an Elastic Load Balancing (ELB) loadbalancer,
    do not create Amazon Route 53 health checks for the EC2 instances. When you register
    anEC2 instance with a load balancer, you configure settings for an ELB health
    check, whichperforms a similar function to an Amazon Route 53 health check.You
    can associate health checks with failover resource record sets in a private hostedzone.
    Note the following:Amazon Route 53 health checkers are outside the VPC. To check
    the health of an endpointwithin a VPC by IP address, you must assign a public
    IP address to the instance in theVPC.You can configure a health checker to check
    the health of an external resource thatthe instance relies on, such as a database
    server.You can create a CloudWatch metric, associate an alarm with the metric,
    and then create ahealth check that is based on the state of the alarm. For example,
    you might create a CloudWatchmetric that checks the status of the Amazon EC2 StatusCheckFailed
    metric, add analarm to the metric, and then create a health check that is based
    on the state of thealarm. For information about creating CloudWatch metrics and
    alarms by using the CloudWatch console,see the Amazon CloudWatch User Guide.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401healthcheck-post-openapi.md
- name: AWS Route 53 API - Create Hosted Zone
  x-api-slug: 20130401hostedzone-post
  description: Creates a new public hosted zone, used to specify how the Domain Name
    System (DNS)routes traffic on the Internet for a domain, such as example.com,
    and its subdomains. ImportantPublic hosted zones can't be converted to a private
    hosted zone or vice versa.Instead, create a new hosted zone with the same name
    and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
    resource. The request body must include a documentwith a CreateHostedZoneRequest
    element. The response returns theCreateHostedZoneResponse element containing metadata
    about the hostedzone.Fore more information about charges for hosted zones, see
    Amazon Route 53 Pricing.Note the following:You can't create a hosted zone for
    a top-level domain (TLD).Amazon Route 53 automatically creates a default SOA record
    and four NS records for the zone.For more information about SOA and NS records,
    see NS and SOA Records that Amazon Route 53 Creates for a Hosted Zone in the Amazon
    Route 53 Developer Guide.If your domain is registered with a registrar other than
    Amazon Route 53, you must update thename servers with your registrar to make Amazon
    Route 53 your DNS service. For more information, seeConfiguring Amazon Route 53
    as your DNSService in the Amazon Route 53 Developer's Guide.After creating a zone,
    its initial status is PENDING. This means that itis not yet available on all DNS
    servers. The status of the zone changes to INSYNCwhen the NS and SOA records are
    available on all Amazon Route 53 DNS servers. When trying to create a hosted zone
    using a reusable delegation set, specify anoptional DelegationSetId, and Amazon
    Route 53 would assign those 4 NS records for the zone, instead ofallotting a new
    one.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzone-post-openapi.md
- name: AWS Route 53 API - Associate V P C With Hosted Zone
  x-api-slug: 20130401hostedzoneidassociatevpc-post
  description: Associates an Amazon VPC with a private hosted zone. ImportantTo perform
    the association, the VPC and the private hosted zone must already exist. You can't
    convert a public hosted zone into a private hosted zone.Send a POST request to
    the /2013-04-01/hostedzone/hosted zone ID/associatevpc resource. The request body
    must include a document with an AssociateVPCWithHostedZoneRequest element. The
    response contains a ChangeInfo data type that you can use to track the progress
    of the request. NoteIf you want to associate a VPC that was created by using one
    AWS account with a private hosted zone that was created by using a different account,
    the AWS account that created the private hosted zone must first submit a CreateVPCAssociationAuthorization
    request. Then the account that created the VPC must submit an AssociateVPCWithHostedZone
    request.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzoneidassociatevpc-post-openapi.md
- name: AWS Route 53 API - Create V P C Association Authorization
  x-api-slug: 20130401hostedzoneidauthorizevpcassociation-post
  description: Authorizes the AWS account that created a specified VPC to submit an
    AssociateVPCWithHostedZone request to associate the VPC with a specified hosted
    zone that was created by a different account. To submit a CreateVPCAssociationAuthorization
    request, you must use the account that created the hosted zone. After you authorize
    the association, use the account that created the VPC to submit an AssociateVPCWithHostedZone
    request.NoteIf you want to associate multiple VPCs that you created by using one
    account with a hosted zone that you created by using a different account, you
    must submit one authorization request for each VPC.Send a POST request to the
    /2013-04-01/hostedzone/hosted zone ID/authorizevpcassociation resource. The request
    body must include a document with a CreateVPCAssociationAuthorizationRequest element.
    The response contains information about the authorization.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzoneidauthorizevpcassociation-post-openapi.md
- name: AWS Route 53 API - Disassociate V P C From Hosted Zone
  x-api-slug: 20130401hostedzoneiddisassociatevpc-post
  description: Disassociates a VPC from a Amazon Route 53 private hosted zone. NoteYou
    can't disassociate the last VPC from a private hosted zone.Send a POST request
    to the /2013-04-01/hostedzone/hosted zone ID/disassociatevpcresource. The request
    body must include a document with a DisassociateVPCFromHostedZoneRequest element.
    The response includes a DisassociateVPCFromHostedZoneResponse element.ImportantYou
    can't disassociate a VPC from a private hosted zone when only one VPC is associated
    with the hosted zone. You also can't convert a private hosted zone into a public
    hosted zone.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzoneiddisassociatevpc-post-openapi.md
- name: AWS Route 53 API - List Resource Record Sets
  x-api-slug: 20130401hostedzoneidrrsetampidentifierstartrecordidentifierampmaxitemsmaxitemsnamestartrecordnameamptypestartrecordtype-get
  description: 'Lists the resource record sets in a specified hosted zone.            ListResourceRecordSets
    returns up to 100 resource record sets at a time in ASCII order, beginning at
    a position specified by the name and type elements. The action sorts results first
    by DNS name with the labels reversed, for example:            com.example.www.         Note
    the trailing dot, which can change the sort order in some circumstances.When multiple
    records have the same DNS name, the action sorts results by the record type.You
    can use the name and type elements to adjust the beginning position of the list
    of resource record sets returned:If you do not specify Name or TypeThe results
    begin with the first resource record set that the hosted zone contains.If you
    specify Name but not TypeThe results begin with the first resource record set
    in the list whose name is greater than or equal to Name.If you specify Type but
    not NameAmazon Route 53 returns the InvalidInput error.If you specify both Name
    and TypeThe results begin with the first resource record set in the list whose
    name is greater than or equal to Name, and whose type is greater than or equal
    to Type.This action returns the most current version of the records. This includes
    records that are PENDING, and that are not yet available on all Amazon Route 53
    DNS servers.To ensure that you get an accurate listing of the resource record
    sets for a hosted zone at a point in time, do not submit a ChangeResourceRecordSets
    request while you''re paging through the results of a ListResourceRecordSets request.
    If you do, some pages may display results without the latest changes while other
    pages display results with the latest changes.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzoneidrrsetampidentifierstartrecordidentifierampmaxitemsmaxitemsnamestartrecordnameamptypestartrecordtype-get-openapi.md
- name: AWS Route 53 API - Change Resource Record Sets
  x-api-slug: 20130401hostedzoneidrrset-post
  description: 'Create, change, update, or delete authoritative DNS information on
    all Amazon Route 53 servers.Send a POST request to:             /2013-04-01/hostedzone/Amazon
    Route 53 hosted ZoneID/rrset resource. The request body must include a document
    with aChangeResourceRecordSetsRequest element. The request body contains a list
    ofchange items, known as a change batch. Change batches are considered transactional
    changes.When using the Amazon Route 53 API to change resource record sets, Amazon
    Route 53 either makes all or none of thechanges in a change batch request. This
    ensures that Amazon Route 53 never partially implements theintended changes to
    the resource record sets in a hosted zone. For example, a change batch request
    that deletes the CNAME record forwww.example.com and creates an alias resource
    record set for www.example.com. Amazon Route 53 deletesthe first resource record
    set and creates the second resource record set in a singleoperation. If either
    the DELETE or the CREATE action fails, thenboth changes (plus any other changes
    in the batch) fail, and the original CNAMErecord continues to exist.ImportantDue
    to the nature of transactional changes, you can''t delete the same resourcerecord
    set more than once in a single change batch. If you attempt to delete the same
    changebatch more than once, Amazon Route 53 returns an InvalidChangeBatch error.NoteTo
    create resource record sets for complex routing configurations, use either thetraffic
    flow visual editor in the Amazon Route 53 console or the API actions for traffic
    policies andtraffic policy instances. Save the configuration as a traffic policy,
    then associate thetraffic policy with one or more domain names (such as example.com)
    or subdomain names (suchas www.example.com), in the same hosted zone or in multiple
    hosted zones. You can roll backthe updates if the new configuration isn''t performing
    as expected. For more information, seeUsing Traffic Flow to Route DNSTraffic in
    the Amazon Route 53 Developer Guide.Use ChangeResourceRecordsSetsRequest to perform
    the following actions:                  CREATE: Creates a resource record set
    that has the specified values.                  DELETE: Deletes an existing resource
    record set that has the specified values.                  UPSERT: If a resource
    record set does not already exist, AWS createsit. If a resource set does exist,
    Amazon Route 53 updates it with the values in the request. The values that you
    need to include in the request depend on the type of resource record set that
    you''re creating, deleting, or updating:            Basic resource record sets
    (excluding alias, failover, geolocation, latency, and weighted resource record
    sets)                           Name                                 Type                                 TTL                           Failover,
    geolocation, latency, or weighted resource record sets (excluding alias resource
    record sets)                           Name                                 Type                                 TTL                                 SetIdentifier                           Alias
    resource record sets (including failover alias, geolocation alias, latency alias,
    and weighted alias resource record sets)                           Name                                 Type                                 AliasTarget
    (includes DNSName, EvaluateTargetHealth, and HostedZoneId)                  SetIdentifier
    (for failover, geolocation, latency, and weighted resource record sets)When you
    submit a ChangeResourceRecordSets request, Amazon Route 53 propagates your changes
    to all of the Amazon Route 53 authoritative DNS servers. While your changes are
    propagating, GetChange returns a status of PENDING. When propagation is complete,
    GetChange returns a status of INSYNC. Changes generally propagate to all Amazon
    Route 53 name servers in a few minutes. In rare circumstances, propagation can
    take up to 30 minutes. For more information, see GetChange       For information
    about the limits on a ChangeResourceRecordSets request, see Limits in the Amazon
    Route 53 Developer Guide.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzoneidrrset-post-openapi.md
- name: AWS Route 53 API - List Hosted Zones By Name
  x-api-slug: 20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get
  description: 'Retrieves a list of your hosted zones in lexicographic order. Send
    a GETrequest to the /2013-04-01/hostedzonesbyname resource. The response includes
    aHostedZones child element for each hosted zone created by the current AWSaccount.             ListHostedZonesByName
    sorts hosted zones by name with the labels reversed.For example:                  com.example.www.               Note
    the trailing dot, which can change the sort order in some circumstances.If the
    domain name includes escape characters or Punycode,ListHostedZonesByName alphabetizes
    the domain name using the escaped orPunycoded value, which is the format that
    Amazon Route 53 saves in its database. For example, to createa hosted zone for
    example.com, specify ex\344mple.com for the domain name.ListHostedZonesByName
    alphabetizes it as:                  com.ex\344mple.               The labels
    are reversed and alphabetized using the escaped value. For more informationabout
    valid domain name formats, including internationalized domain names, see DNS Domain
    Name Format in theAmazon Route 53 Developer Guide.Amazon Route 53 returns up to
    100 items in each response. If you have a lot of hosted zones, usethe MaxItems
    parameter to list them in groups of up to 100. The response includesvalues that
    help navigate from one group of MaxItems hosted zones to thenext:The DNSName and
    HostedZoneId elements in the responsecontain the values, if any, specified for
    the dnsname andhostedzoneid parameters in the request that produced the currentresponse.The
    MaxItems element in the response contains the value, if any, thatyou specified
    for the maxitems parameter in the request that produced thecurrent response.If
    the value of IsTruncated in the response is true, there are morehosted zones associated
    with the current AWS account. If IsTruncated is false, this response includes
    the last hosted zonethat is associated with the current account. The NextDNSName
    element andNextHostedZoneId elements are omitted from the response.The NextDNSName
    and NextHostedZoneId elements in theresponse contain the domain name and the hosted
    zone ID of the next hosted zone that isassociated with the current AWS account.
    If you want to list more hosted zones, makeanother call to ListHostedZonesByName,
    and specify the value ofNextDNSName and NextHostedZoneId in the dnsnameand hostedzoneid
    parameters, respectively.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get-openapi.md
- name: AWS Route 53 API - Delete Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstanceid-delete
  description: Deletes a traffic policy instance and all of the resource record sets
    that Amazon Route 53created when you created the instance.Send a DELETE request
    to the /Amazon Route 53 APIversion/trafficpolicy/traffic policy instance ID            resource.NoteIn
    the Amazon Route 53 console, traffic policy instances are known as policy records.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401trafficpolicyinstanceid-delete-openapi.md
- name: AWS Route 53 API - Get Traffic Policy Instance
  x-api-slug: 20130401trafficpolicyinstanceid-get
  description: Gets information about a specified traffic policy instance.Send a GET
    request to the /Amazon Route 53 APIversion/trafficpolicyinstance resource.NoteAfter
    you submit a CreateTrafficPolicyInstance or anUpdateTrafficPolicyInstance request,
    there's a brief delay while Amazon Route 53creates the resource record sets that
    are specified in the traffic policy definition. Formore information, see the State
    response element.NoteIn the Amazon Route 53 console, traffic policy instances
    are known as policy records.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401trafficpolicyinstanceid-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances By Hosted Zone
  x-api-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource and include the ID of the hostedzone.Amazon Route 53 returns a maximum
    of 100 items in each response. If you have a lot of trafficpolicy instances, you
    can use the MaxItems parameter to list them in groups of upto 100.The response
    includes four values that help you navigate from one group ofMaxItems traffic
    policy instances to the next:             IsTruncated               If the value
    of IsTruncated in the response is true, there aremore traffic policy instances
    associated with the current AWS account.If IsTruncated is false, this response
    includes the lasttraffic policy instance that is associated with the current account.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these two values in the responserepresent the first traffic
    policy instance in the next group of MaxItemstraffic policy instances. To list
    more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
    and specify these values in thecorresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances By Policy
  x-api-slug: 20130401trafficpolicyinstancestrafficpolicyamphostedzoneidhostedzoneidmarkeridtrafficpolicyidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    by using a specifytraffic policy version.NoteAfter you submit a CreateTrafficPolicyInstance
    or anUpdateTrafficPolicyInstance request, there''s a brief delay while Amazon
    Route 53creates the resource record sets that are specified in the traffic policy
    definition. Formore information, see the State response element.Send a GET request
    to the /Route 53 APIversion/trafficpolicyinstance resource and include the ID
    and version ofthe traffic policy.Amazon Route 53 returns a maximum of 100 items
    in each response. If you have a lot of trafficpolicy instances, you can use the
    MaxItems parameter to list them in groups of upto 100.The response includes five
    values that help you navigate from one group ofMaxItems traffic policy instances
    to the next:             IsTruncated               If the value of IsTruncated
    in the response is true,there are more traffic policy instances associated with
    the specified trafficpolicy.If IsTruncated is false, this response includes the
    lasttraffic policy instance that is associated with the specified traffic policy.             MaxItems               The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  HostedZoneIdMarker, TrafficPolicyInstanceNameMarker,
    and TrafficPolicyInstanceTypeMarker               If IsTruncated is true, these
    values in the responserepresent the first traffic policy instance in the next
    group of MaxItemstraffic policy instances. To list more traffic policy instances,
    make another call toListTrafficPolicyInstancesByPolicy, and specify these values
    in thecorresponding request parameters.If IsTruncated is false, all three elements
    are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401trafficpolicyinstancestrafficpolicyamphostedzoneidhostedzoneidmarkeridtrafficpolicyidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
- name: AWS Route 53 API - List Traffic Policy Instances
  x-api-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidmarkerampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
  description: 'Gets information about the traffic policy instances that you created
    by using thecurrent AWS account.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource.Amazon Route 53 returns a maximum of 100 items in each response. If you
    have a lot of trafficpolicy instances, you can use the MaxItems parameter to list
    them in groups of upto 100.The response includes five values that help you navigate
    from one group ofMaxItems traffic policy instances to the next:             IsTruncated           If
    the value of IsTruncated in the response is true,there are more traffic policy
    instances associated with the current AWSaccount.If IsTruncated is false, this
    response includes the lasttraffic policy instance that is associated with the
    current account.             MaxItems           The value that you specified for
    the MaxItems parameter in the requestthat produced the current response.                  HostedZoneIdMarker,
    TrafficPolicyInstanceNameMarker, and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these three values in theresponse represent the first traffic
    policy instance in the next group ofMaxItems traffic policy instances. To list
    more traffic policy instances,make another call to ListTrafficPolicyInstances,
    and specify these values inthe corresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Networking_AmazonRoute53.png
  humanURL: https://aws.amazon.com/route53/
  baseURL: :///
  tags: Amazon Web Services, DNS, API Service Provider, API Service Provider, API
    Provider, Profiles, Relative Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/notes/master/_listings/aws-route-53/20130401trafficpolicyinstanceshostedzoneidhostedzoneidmarkerampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://aws.rekognition.api.gallery.streamdata.io
- type: x-api-stack
  url: http://aws.route.53.stack.network
- type: x-documentation
  url: http://docs.aws.amazon.com/Route53/latest/APIReference/
- type: x-faq
  url: https://aws.amazon.com/route53/faqs/
- type: x-forum
  url: https://forums.aws.amazon.com/forum.jspa?forumID=87
- type: x-pricing
  url: https://aws.amazon.com/route53/pricing/
- type: x-registrar-policies
  url: https://aws.amazon.com/route53/amazon-registrar-policies/
- type: x-service-health
  url: http://status.aws.amazon.com/
- type: x-service-level-agreement
  url: https://aws.amazon.com/route53/sla
- type: x-sla
  url: https://aws.amazon.com/route53/sla/
- type: x-website
  url: https://aws.amazon.com/route53/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---