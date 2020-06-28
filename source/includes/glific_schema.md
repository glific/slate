# Schema Types

<details>
  <summary><strong>Table of Contents</strong></summary>

  * [Query](#query)
  * [Mutation](#mutation)
  * [Objects](#objects)
    * [Contact](#contact)
    * [ContactGroup](#contactgroup)
    * [ContactGroupResult](#contactgroupresult)
    * [ContactResult](#contactresult)
    * [ContactTag](#contacttag)
    * [ContactTagResult](#contacttagresult)
    * [Conversation](#conversation)
    * [Group](#group)
    * [GroupResult](#groupresult)
    * [InputError](#inputerror)
    * [Language](#language)
    * [LanguageResult](#languageresult)
    * [Message](#message)
    * [MessageMedia](#messagemedia)
    * [MessageMediaResult](#messagemediaresult)
    * [MessageResult](#messageresult)
    * [MessageTag](#messagetag)
    * [MessageTagResult](#messagetagresult)
    * [Organization](#organization)
    * [OrganizationResult](#organizationresult)
    * [Provider](#provider)
    * [ProviderResult](#providerresult)
    * [RootSubscriptionType](#rootsubscriptiontype)
    * [SavedSearch](#savedsearch)
    * [SavedSearchResult](#savedsearchresult)
    * [SessionTemplate](#sessiontemplate)
    * [SessionTemplateResult](#sessiontemplateresult)
    * [Tag](#tag)
    * [TagResult](#tagresult)
    * [User](#user)
    * [UserGroup](#usergroup)
    * [UserGroupResult](#usergroupresult)
    * [UserResult](#userresult)
  * [Inputs](#inputs)
    * [ContactFilter](#contactfilter)
    * [ContactGroupInput](#contactgroupinput)
    * [ContactInput](#contactinput)
    * [ContactTagInput](#contacttaginput)
    * [ConversationFilter](#conversationfilter)
    * [ConversationsFilter](#conversationsfilter)
    * [GroupFilter](#groupfilter)
    * [GroupInput](#groupinput)
    * [LanguageInput](#languageinput)
    * [MessageFilter](#messagefilter)
    * [MessageInput](#messageinput)
    * [MessageMediaInput](#messagemediainput)
    * [MessageTagInput](#messagetaginput)
    * [MessageToTemplateInput](#messagetotemplateinput)
    * [Opts](#opts)
    * [OrganizationFilter](#organizationfilter)
    * [OrganizationInput](#organizationinput)
    * [ProviderFilter](#providerfilter)
    * [ProviderInput](#providerinput)
    * [RegistrationInput](#registrationinput)
    * [SavedSearchFilters](#savedsearchfilters)
    * [SavedSearchInput](#savedsearchinput)
    * [SearchFilter](#searchfilter)
    * [SessionTemplateFilter](#sessiontemplatefilter)
    * [SessionTemplateInput](#sessiontemplateinput)
    * [TagFilter](#tagfilter)
    * [TagInput](#taginput)
    * [UserFilter](#userfilter)
    * [UserGroupInput](#usergroupinput)
    * [UserInput](#userinput)
  * [Enums](#enums)
    * [ContactStatusEnum](#contactstatusenum)
    * [MessageFlowEnum](#messageflowenum)
    * [MessageStatusEnum](#messagestatusenum)
    * [MessageTypesEnum](#messagetypesenum)
    * [SortOrder](#sortorder)
  * [Scalars](#scalars)
    * [Boolean](#boolean)
    * [DateTime](#datetime)
    * [Gid](#gid)
    * [ID](#id)
    * [Int](#int)
    * [Json](#json)
    * [String](#string)

</details>

## Query (RootQueryType)
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>organizations</strong></td>
<td valign="top">[<a href="#organization">Organization</a>]</td>
<td>

Get a list of all organizations filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#organizationfilter">OrganizationFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">order</td>
<td valign="top"><a href="#sortorder">SortOrder</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>users</strong></td>
<td valign="top">[<a href="#user">User</a>]</td>
<td>

Get a list of all users filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#userfilter">UserFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countMessagesMedia</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all message media

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conversations</strong></td>
<td valign="top">[<a href="#conversation">Conversation</a>]</td>
<td>

get the conversations

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">contactOpts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#conversationsfilter">ConversationsFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">messageOpts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contacts</strong></td>
<td valign="top">[<a href="#contact">Contact</a>]</td>
<td>

Get a list of all contacts filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#contactfilter">ContactFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messagesMedia</strong></td>
<td valign="top">[<a href="#messagemedia">MessageMedia</a>]</td>
<td>

Get a list of all message_media

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countTags</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all tags filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#tagfilter">TagFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#organizationresult">OrganizationResult</a></td>
<td>

get the details of one organization

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countSessionTemplates</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all session_templates filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#sessiontemplatefilter">SessionTemplateFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countUsers</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all users filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#userfilter">UserFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>search</strong></td>
<td valign="top">[<a href="#conversation">Conversation</a>]</td>
<td>

Search for conversations

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">contactOpts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#searchfilter">SearchFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">messageOpts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">term</td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#languageresult">LanguageResult</a></td>
<td>

get the details of one language

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>savedSearches</strong></td>
<td valign="top">[<a href="#savedsearch">SavedSearch</a>]</td>
<td>

Get a list of all searches

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#savedsearchfilters">SavedSearchFilters</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#tag">Tag</a>]</td>
<td>

Get a list of all tags filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#tagfilter">TagFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#tagresult">TagResult</a></td>
<td>

get the details of one tag

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countMessages</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all messages filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#messagefilter">MessageFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countGroups</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all groups filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#groupfilter">GroupFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sessionTemplate</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td>

get the details of one session_template

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groups</strong></td>
<td valign="top">[<a href="#group">Group</a>]</td>
<td>

Get a list of all groups filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#groupfilter">GroupFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providers</strong></td>
<td valign="top">[<a href="#provider">Provider</a>]</td>
<td>

Get a list of all providers filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#providerfilter">ProviderFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">order</td>
<td valign="top"><a href="#sortorder">SortOrder</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countContacts</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all contacts filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#contactfilter">ContactFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messageMedia</strong></td>
<td valign="top"><a href="#messagemediaresult">MessageMediaResult</a></td>
<td>

get the details of one message media

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countOrganizations</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all organizations filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#organizationfilter">OrganizationFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>conversation</strong></td>
<td valign="top"><a href="#conversation">Conversation</a></td>
<td>

get the details of conversation with one user

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">contactId</td>
<td valign="top"><a href="#gid">Gid</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#conversationfilter">ConversationFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">messageOpts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contactresult">ContactResult</a></td>
<td>

get the details of one contact

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sessionTemplates</strong></td>
<td valign="top">[<a href="#sessiontemplate">SessionTemplate</a>]</td>
<td>

Get a list of all session_templates filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#sessiontemplatefilter">SessionTemplateFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">order</td>
<td valign="top"><a href="#sortorder">SortOrder</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td>

get the details of one message

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provider</strong></td>
<td valign="top"><a href="#providerresult">ProviderResult</a></td>
<td>

get the details of one provider

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>savedSearch</strong></td>
<td valign="top"><a href="#savedsearchresult">SavedSearchResult</a></td>
<td>

get the details of one saved search

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countProviders</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all providers filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#providerfilter">ProviderFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languages</strong></td>
<td valign="top">[<a href="#language">Language</a>]</td>
<td>

Get a list of all languages filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>countLanguages</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Get a count of all languages

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#groupresult">GroupResult</a></td>
<td>

get the details of one group

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messages</strong></td>
<td valign="top">[<a href="#message">Message</a>]</td>
<td>

Get a list of all messages filtered by various criteria

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">filter</td>
<td valign="top"><a href="#messagefilter">MessageFilter</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">opts</td>
<td valign="top"><a href="#opts">Opts</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#userresult">UserResult</a></td>
<td>

get the details of one user

</td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Mutation (RootMutationType)
<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>updateMessageMedia</strong></td>
<td valign="top"><a href="#messagemediaresult">MessageMediaResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messagemediainput">MessageMediaInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSavedSearch</strong></td>
<td valign="top"><a href="#savedsearchresult">SavedSearchResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendSessionMessage</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">receiverId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteUser</strong></td>
<td valign="top"><a href="#userresult">UserResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createMessageMedia</strong></td>
<td valign="top"><a href="#messagemediaresult">MessageMediaResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messagemediainput">MessageMediaInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateTag</strong></td>
<td valign="top"><a href="#tagresult">TagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#taginput">TagInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createGroup</strong></td>
<td valign="top"><a href="#groupresult">GroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#groupinput">GroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteMessageMedia</strong></td>
<td valign="top"><a href="#messagemediaresult">MessageMediaResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteMessage</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteProvider</strong></td>
<td valign="top"><a href="#providerresult">ProviderResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createMessageTag</strong></td>
<td valign="top"><a href="#messagetagresult">MessageTagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messagetaginput">MessageTagInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateProvider</strong></td>
<td valign="top"><a href="#providerresult">ProviderResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#providerinput">ProviderInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSessionTemplate</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#sessiontemplateinput">SessionTemplateInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createLanguage</strong></td>
<td valign="top"><a href="#languageresult">LanguageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#languageinput">LanguageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createUserGroup</strong></td>
<td valign="top"><a href="#usergroupresult">UserGroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#usergroupinput">UserGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteContact</strong></td>
<td valign="top"><a href="#contactresult">ContactResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendMessage</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTag</strong></td>
<td valign="top"><a href="#tagresult">TagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#taginput">TagInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateMessage</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messageinput">MessageInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createProvider</strong></td>
<td valign="top"><a href="#providerresult">ProviderResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#providerinput">ProviderInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteContactTag</strong></td>
<td valign="top"><a href="#contacttagresult">ContactTagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateContact</strong></td>
<td valign="top"><a href="#contactresult">ContactResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#contactinput">ContactInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateLanguage</strong></td>
<td valign="top"><a href="#languageresult">LanguageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#languageinput">LanguageInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteGroup</strong></td>
<td valign="top"><a href="#groupresult">GroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createContact</strong></td>
<td valign="top"><a href="#contactresult">ContactResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#contactinput">ContactInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteSessionTemplate</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteOrganization</strong></td>
<td valign="top"><a href="#organizationresult">OrganizationResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createMessage</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messageinput">MessageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateUser</strong></td>
<td valign="top"><a href="#userresult">UserResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#userinput">UserInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateOrganization</strong></td>
<td valign="top"><a href="#organizationresult">OrganizationResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#organizationinput">OrganizationInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createAndSendMessage</strong></td>
<td valign="top"><a href="#messageresult">MessageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messageinput">MessageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteContactGroup</strong></td>
<td valign="top"><a href="#contactgroupresult">ContactGroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createContactGroup</strong></td>
<td valign="top"><a href="#contactgroupresult">ContactGroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#contactgroupinput">ContactGroupInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSavedSearch</strong></td>
<td valign="top"><a href="#savedsearchresult">SavedSearchResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#savedsearchinput">SavedSearchInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteMessageTag</strong></td>
<td valign="top"><a href="#messagetagresult">MessageTagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createAndSendMessageToContacts</strong></td>
<td valign="top">[<a href="#message">Message</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">contactIds</td>
<td valign="top">[<a href="#id">ID</a>]!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messageinput">MessageInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createTemplateFormMessage</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#messagetotemplateinput">MessageToTemplateInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">messageId</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateSavedSearch</strong></td>
<td valign="top"><a href="#savedsearchresult">SavedSearchResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#savedsearchinput">SavedSearchInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updateGroup</strong></td>
<td valign="top"><a href="#groupresult">GroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#groupinput">GroupInput</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createSessionTemplate</strong></td>
<td valign="top"><a href="#sessiontemplateresult">SessionTemplateResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#sessiontemplateinput">SessionTemplateInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteUserGroup</strong></td>
<td valign="top"><a href="#usergroupresult">UserGroupResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sendOtp</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#registrationinput">RegistrationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createOrganization</strong></td>
<td valign="top"><a href="#organizationresult">OrganizationResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#organizationinput">OrganizationInput</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteLanguage</strong></td>
<td valign="top"><a href="#languageresult">LanguageResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deleteTag</strong></td>
<td valign="top"><a href="#tagresult">TagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">id</td>
<td valign="top"><a href="#id">ID</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>createContactTag</strong></td>
<td valign="top"><a href="#contacttagresult">ContactTagResult</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" align="right" valign="top">input</td>
<td valign="top"><a href="#contacttaginput">ContactTagInput</a>!</td>
<td></td>
</tr>
</tbody>
</table>

## Objects

### Contact

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optinTime</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>optoutTime</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#tag">Tag</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### ContactGroup

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ContactGroupResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactGroup</strong></td>
<td valign="top"><a href="#contactgroup">ContactGroup</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### ContactResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### ContactTag

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#tag">Tag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ContactTagResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactTag</strong></td>
<td valign="top"><a href="#contacttag">ContactTag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### Conversation

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messages</strong></td>
<td valign="top">[<a href="#message">Message</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### Group

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isRestricted</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### GroupResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
</tbody>
</table>

### InputError

An error encountered trying to persist input

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>key</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### Language

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelLocale</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>locale</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### LanguageResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#language">Language</a></td>
<td></td>
</tr>
</tbody>
</table>

### Message

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>flow</strong></td>
<td valign="top"><a href="#messageflowenum">MessageFlowEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>insertedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>media</strong></td>
<td valign="top"><a href="#messagemedia">MessageMedia</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerMessageId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#messagestatusenum">MessageStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receiver</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sender</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tags</strong></td>
<td valign="top">[<a href="#tag">Tag</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#messagetypesenum">MessageTypesEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>updatedAt</strong></td>
<td valign="top"><a href="#datetime">DateTime</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageMedia

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>caption</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerMediaId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageMediaResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messageMedia</strong></td>
<td valign="top"><a href="#messagemedia">MessageMedia</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#message">Message</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageTag

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>message</strong></td>
<td valign="top"><a href="#message">Message</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#tag">Tag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageTagResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messageTag</strong></td>
<td valign="top"><a href="#messagetag">MessageTag</a></td>
<td></td>
</tr>
</tbody>
</table>

### Organization

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contact</strong></td>
<td valign="top"><a href="#contact">Contact</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contactName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#language">Language</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provider</strong></td>
<td valign="top"><a href="#provider">Provider</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerKey</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### OrganizationResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>organization</strong></td>
<td valign="top"><a href="#organization">Organization</a></td>
<td></td>
</tr>
</tbody>
</table>

### Provider

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>apiEndPoint</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ProviderResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provider</strong></td>
<td valign="top"><a href="#provider">Provider</a></td>
<td></td>
</tr>
</tbody>
</table>

### RootSubscriptionType

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>createdMessageTag</strong></td>
<td valign="top"><a href="#messagetag">MessageTag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>deletedMessageTag</strong></td>
<td valign="top"><a href="#messagetag">MessageTag</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receivedMessage</strong></td>
<td valign="top"><a href="#message">Message</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sentMessage</strong></td>
<td valign="top"><a href="#message">Message</a></td>
<td></td>
</tr>
</tbody>
</table>

### SavedSearch

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>args</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SavedSearchResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>savedSearch</strong></td>
<td valign="top"><a href="#savedsearch">SavedSearch</a></td>
<td></td>
</tr>
</tbody>
</table>

### SessionTemplate

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isSource</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#language">Language</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>messageMedia</strong></td>
<td valign="top"><a href="#messagemedia">MessageMedia</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parent</strong></td>
<td valign="top"><a href="#sessiontemplate">SessionTemplate</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shortcode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#messagetypesenum">MessageTypesEnum</a></td>
<td></td>
</tr>
</tbody>
</table>

### SessionTemplateResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sessionTemplate</strong></td>
<td valign="top"><a href="#sessiontemplate">SessionTemplate</a></td>
<td></td>
</tr>
</tbody>
</table>

### Tag

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>keywords</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#language">Language</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parent</strong></td>
<td valign="top"><a href="#tag">Tag</a></td>
<td></td>
</tr>
</tbody>
</table>

### TagResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tag</strong></td>
<td valign="top"><a href="#tag">Tag</a></td>
<td></td>
</tr>
</tbody>
</table>

### User

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>roles</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
</tbody>
</table>

### UserGroup

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>group</strong></td>
<td valign="top"><a href="#group">Group</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>value</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserGroupResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userGroup</strong></td>
<td valign="top"><a href="#usergroup">UserGroup</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserResult

<table>
<thead>
<tr>
<th align="left">Field</th>
<th align="right">Argument</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>errors</strong></td>
<td valign="top">[<a href="#inputerror">InputError</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>user</strong></td>
<td valign="top"><a href="#user">User</a></td>
<td></td>
</tr>
</tbody>
</table>

## Inputs

### ContactFilter

Filtering options for contacts

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the phone

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td>

Match the status

</td>
</tr>
</tbody>
</table>

### ContactGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### ContactInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>status</strong></td>
<td valign="top"><a href="#contactstatusenum">ContactStatusEnum</a></td>
<td></td>
</tr>
</tbody>
</table>

### ContactTagInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tagId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### ConversationFilter

Filtering options for conversations

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>excludeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Exclude conversations with these tags

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Include conversations with these tags

</td>
</tr>
</tbody>
</table>

### ConversationsFilter

Filtering options for conversations

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>excludeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Exclude conversations with these tags

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>id</strong></td>
<td valign="top"><a href="#gid">Gid</a></td>
<td>

Match one contact ID

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>ids</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Match multiple contact ids

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Include conversations with these tags

</td>
</tr>
</tbody>
</table>

### GroupFilter

Filtering options for groups

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the label

</td>
</tr>
</tbody>
</table>

### GroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>isRestricted</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### LanguageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>labelLocale</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>locale</strong></td>
<td valign="top"><a href="#string">String</a>!</td>
<td></td>
</tr>
</tbody>
</table>

### MessageFilter

Filtering options for messages

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the namebody

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>either</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the phone with either the sender or receiver

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#messagestatusenum">MessageStatusEnum</a></td>
<td>

Match the status

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receiver</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the receiver

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sender</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the sender

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tagsExcluded</strong></td>
<td valign="top">[<a href="#id">ID</a>]</td>
<td>

Match the tags excluded

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tagsIncluded</strong></td>
<td valign="top">[<a href="#id">ID</a>]</td>
<td>

Match the tags included

</td>
</tr>
</tbody>
</table>

### MessageInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>flow</strong></td>
<td valign="top"><a href="#messageflowenum">MessageFlowEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>mediaId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerMessageId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerStatus</strong></td>
<td valign="top"><a href="#messagestatusenum">MessageStatusEnum</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>receiverId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>senderId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#messagetypesenum">MessageTypesEnum</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageMediaInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>caption</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerMediaId</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>sourceUrl</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>thumbnail</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageTagInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>messageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>tagId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### MessageToTemplateInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shortcode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### Opts

Lets collapse sort order, limit and offset into its own little groups

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>limit</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>offset</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>order</strong></td>
<td valign="top"><a href="#sortorder">SortOrder</a></td>
<td></td>
</tr>
</tbody>
</table>

### OrganizationFilter

Filtering options for organizations

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the contact name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguage</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the default language

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the display name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the email

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>provider</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the provider

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the whatsapp number of organization

</td>
</tr>
</tbody>
</table>

### OrganizationInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>contactId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>contactName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>defaultLanguageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>displayName</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>email</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerKey</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>providerNumber</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### ProviderFilter

Filtering options for providers

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the url of provider

</td>
</tr>
</tbody>
</table>

### ProviderInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>apiEndPoint</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>url</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### RegistrationInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>password</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SavedSearchFilters

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SavedSearchInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>args</strong></td>
<td valign="top"><a href="#json">Json</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
</tbody>
</table>

### SearchFilter

Filtering options for search

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>excludeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Exclude conversations with these tags

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>includeTags</strong></td>
<td valign="top">[<a href="#gid">Gid</a>]</td>
<td>

Include conversations with these tags

</td>
</tr>
</tbody>
</table>

### SessionTemplateFilter

Filtering options for session_templates

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the body of template

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>

Match the active flag

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>

Match the reserved flag

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the label

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match a language

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageId</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Match a language id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parent</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the parent

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentId</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Match the parent

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shortcode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the shortcode of template

</td>
</tr>
</tbody>
</table>

### SessionTemplateInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>body</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isSource</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>shortcode</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>type</strong></td>
<td valign="top"><a href="#messagetypesenum">MessageTypesEnum</a></td>
<td></td>
</tr>
</tbody>
</table>

### TagFilter

Filtering options for tags

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the description

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>

Match the active flag

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td>

Match the reserved flag

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the label

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>language</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match a language

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageId</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Match a language id

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parent</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the parent

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>parentId</strong></td>
<td valign="top"><a href="#int">Int</a></td>
<td>

Match the parent

</td>
</tr>
</tbody>
</table>

### TagInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>description</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isActive</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>isReserved</strong></td>
<td valign="top"><a href="#boolean">Boolean</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>keywords</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>label</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>languageId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserFilter

Filtering options for users

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the name

</td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>phone</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td>

Match the phone

</td>
</tr>
</tbody>
</table>

### UserGroupInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>groupId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>userId</strong></td>
<td valign="top"><a href="#id">ID</a></td>
<td></td>
</tr>
</tbody>
</table>

### UserInput

<table>
<thead>
<tr>
<th colspan="2" align="left">Field</th>
<th align="left">Type</th>
<th align="left">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2" valign="top"><strong>name</strong></td>
<td valign="top"><a href="#string">String</a></td>
<td></td>
</tr>
<tr>
<td colspan="2" valign="top"><strong>roles</strong></td>
<td valign="top">[<a href="#string">String</a>]</td>
<td></td>
</tr>
</tbody>
</table>

## Enums

### ContactStatusEnum

The Contact Status enum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>FAILED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>INVALID</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>PROCESSING</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VALID</strong></td>
<td></td>
</tr>
</tbody>
</table>

### MessageFlowEnum

The Message Flow enum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>INBOUND</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>OUTBOUND</strong></td>
<td></td>
</tr>
</tbody>
</table>

### MessageStatusEnum

The Message Status enum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>DELIVERED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ENQUEUED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>ERROR</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>READ</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>RECEIVED</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>SENT</strong></td>
<td></td>
</tr>
</tbody>
</table>

### MessageTypesEnum

The Message Types enum

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>AUDIO</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>CONTACT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DOCUMENT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>HSM</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>IMAGE</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>LOCATION</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>TEXT</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>VIDEO</strong></td>
<td></td>
</tr>
</tbody>
</table>

### SortOrder

Enum for ordering results

<table>
<thead>
<th align="left">Value</th>
<th align="left">Description</th>
</thead>
<tbody>
<tr>
<td valign="top"><strong>ASC</strong></td>
<td></td>
</tr>
<tr>
<td valign="top"><strong>DESC</strong></td>
<td></td>
</tr>
</tbody>
</table>

## Scalars

### Boolean

The `Boolean` scalar type represents `true` or `false`.

### DateTime

The `DateTime` scalar type represents a date and time in the UTC
timezone. The DateTime appears in a JSON response as an ISO8601 formatted
string, including UTC timezone ("Z"). The parsed date and time string will
be converted to UTC if there is an offset.

### Gid

The `gid` scalar appears in JSON as a String. The string appears to
the glific backend as an integer

### ID

The `ID` scalar type represents a unique identifier, often used to
refetch an object or as key for a cache. The ID type appears in a JSON
response as a String; however, it is not intended to be human-readable.
When expected as an input type, any string (such as `"4"`) or integer
(such as `4`) input value will be accepted as an ID.

### Int

The `Int` scalar type represents non-fractional signed whole numeric values.
Int can represent values between `-(2^53 - 1)` and `2^53 - 1` since it is
represented in JSON as double-precision floating point numbers specified
by [IEEE 754](http://en.wikipedia.org/wiki/IEEE_floating_point).

### Json

A generic json type so return the results as json object

### String

The `String` scalar type represents textual data, represented as UTF-8
character sequences. The String type is most often used by GraphQL to
represent free-form human-readable text.

