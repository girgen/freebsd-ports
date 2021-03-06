# Created by: Torsten Zuehlsdorff <tz@FreeBSD.org>
# $FreeBSD$

PORTNAME=	gitlab
PORTVERSION=	8.11.11
DISTVERSIONPREFIX=	v
PORTREVISION=	1
CATEGORIES=	www devel

MAINTAINER=	tz@FreeBSD.org
COMMENT=	Web GUI for managing git repositories

LICENSE=	MIT
LICENSE_FILE=	${WRKSRC}/LICENSE

BUILD_DEPENDS=	gem:devel/ruby-gems

# the rubygems of RUN_DEPENDS matches the order of the Gemfile
# which makes maintaining this long list much easier!
RUN_DEPENDS=	git>=2.7.4:devel/git \
	gitlab-shell>=3.4.0:devel/gitlab-shell\
	gitlab-workhorse>=0.7.11:www/gitlab-workhorse \
	redis>=2.8.23:databases/redis \
	rubygem-rails4>=4.2.7.1:www/rubygem-rails4 \
	rubygem-rails-deprecated_sanitizer>=1.0.3:devel/rubygem-rails-deprecated_sanitizer \
	rubygem-responders>=2.0:www/rubygem-responders \
	rubygem-sprockets3>=3.6:devel/rubygem-sprockets3 \
	rubygem-sprockets-es6>=0:devel/rubygem-sprockets-es6 \
	rubygem-default_value_for>=3.0.1:devel/rubygem-default_value_for \
	rubygem-pg>=0.18.2:databases/rubygem-pg \
	rubygem-devise>=4.0:devel/rubygem-devise \
	rubygem-doorkeeper>=4.2:security/rubygem-doorkeeper \
	rubygem-omniauth>=1.3.1:security/rubygem-omniauth \
	rubygem-omniauth-auth0>=1.4.1:net/rubygem-omniauth-auth0 \
	rubygem-omniauth-azure-oauth2>=0.0.6:net/rubygem-omniauth-azure-oauth2 \
	rubygem-omniauth-bitbucket>=0.0.2:security/rubygem-omniauth-bitbucket \
	rubygem-omniauth-cas3>=1.1.2:security/rubygem-omniauth-cas3 \
	rubygem-omniauth-facebook>=3.0.0:net/rubygem-omniauth-facebook \
	rubygem-omniauth-github>=1.1.1:net/rubygem-omniauth-github \
	rubygem-omniauth-gitlab>=1.0.0:security/rubygem-omniauth-gitlab \
	rubygem-omniauth-google-oauth2>=0.4.1:net/rubygem-omniauth-google-oauth2 \
	rubygem-omniauth-saml>=1.6.0:security/rubygem-omniauth-saml \
	rubygem-omniauth-shibboleth>=1.2.0:security/rubygem-omniauth-shibboleth \
	rubygem-omniauth-twitter>=1.2.0:net/rubygem-omniauth-twitter \
	rubygem-omniauth_crowd>=2.2.0:devel/rubygem-omniauth_crowd \
	rubygem-rack-oauth2>=1.2.1:security/rubygem-rack-oauth2 \
	rubygem-jwt>=1.0:www/rubygem-jwt \
	rubygem-recaptcha>=3.0:devel/rubygem-recaptcha \
	rubygem-akismet>=2.0:devel/rubygem-akismet \
	rubygem-devise-two-factor>=3.0.0:security/rubygem-devise-two-factor \
	rubygem-rqrcode-rails3>=0.1.7:www/rubygem-rqrcode-rails3 \
	rubygem-attr_encrypted>=3.0.0:security/rubygem-attr_encrypted \
	rubygem-u2f>=0.2.1:net/rubygem-u2f \
	rubygem-browser>=2.2:www/rubygem-browser \
	rubygem-gitlab_git>=10.5:devel/rubygem-gitlab_git \
	rubygem-gitlab_omniauth-ldap>=1.2.1:net/rubygem-gitlab_omniauth-ldap \
	rubygem-gollum-lib>=4.2.0:www/rubygem-gollum-lib \
	rubygem-gollum-rugged_adapter>=0.4.2:www/rubygem-gollum-rugged_adapter \
	rubygem-github-linguist>=4.7.0:textproc/rubygem-github-linguist \
	rubygem-grape>=0.15.0:devel/rubygem-grape \
	rubygem-grape-entity>=0.4.2:devel/rubygem-grape-entity \
	rubygem-rack-cors>=0.4.0:www/rubygem-rack-cors \
	rubygem-kaminari-rails4>=0.17.0:www/rubygem-kaminari-rails4 \
	rubygem-hamlit>=2.6.1:www/rubygem-hamlit \
	rubygem-carrierwave>=0.10.0:www/rubygem-carrierwave \
	rubygem-dropzonejs-rails>=0.7.1:www/rubygem-dropzonejs-rails \
	rubygem-fog-aws>=0.9:net/rubygem-fog-aws \
	rubygem-fog-azure>=0.0:net/rubygem-fog-azure \
	rubygem-fog-core>=1.40:devel/rubygem-fog-core \
	rubygem-fog-local>=0.3:net/rubygem-fog-local \
	rubygem-fog-google>=0.3:net/rubygem-fog-google \
	rubygem-fog-openstack>=0.1:net/rubygem-fog-openstack \
	rubygem-fog-rackspace>=0.1.1:net/rubygem-fog-rackspace \
	rubygem-unf>=0.1.4:textproc/rubygem-unf \
	rubygem-six>=0.2.0:security/rubygem-six \
	rubygem-seed-fu>=2.3.5:databases/rubygem-seed-fu \
	rubygem-html-pipeline1>=1.11.0:textproc/rubygem-html-pipeline1 \
	rubygem-task_list>=1.0.2:www/rubygem-task_list \
	rubygem-github-markup>=1.4:textproc/rubygem-github-markup \
	rubygem-redcarpet>=3.3.3:textproc/rubygem-redcarpet \
	rubygem-redcloth>=4.3.2:www/rubygem-redcloth \
	rubygem-rdoc>=3.6:devel/rubygem-rdoc \
	rubygem-org-ruby>=0.9.12:textproc/rubygem-org-ruby \
	rubygem-creole>=0.5.0:textproc/rubygem-creole \
	rubygem-wikicloth>=0.8.1:textproc/rubygem-wikicloth \
	rubygem-asciidoctor>=1.5.2:textproc/rubygem-asciidoctor \
	rubygem-rouge>=2.0:textproc/rubygem-rouge \
	rubygem-nokogiri>=1.6.7.2:textproc/rubygem-nokogiri  \
	rubygem-diffy>=3.0.3:textproc/rubygem-diffy \
	rubygem-unicorn>=4.9.0:www/rubygem-unicorn \
	rubygem-unicorn-worker-killer>=0.4.2:www/rubygem-unicorn-worker-killer \
	rubygem-state_machines-activerecord>=0.4.0:databases/rubygem-state_machines-activerecord \
	rubygem-after_commit_queue>=1.3.0:databases/rubygem-after_commit_queue \
	rubygem-acts-as-taggable-on3>=3.4.0:www/rubygem-acts-as-taggable-on3 \
	rubygem-sinatra>=1.4.4:www/rubygem-sinatra \
	rubygem-sidekiq>=4.0:devel/rubygem-sidekiq \
	rubygem-sidekiq-cron>=0.4.0:devel/rubygem-sidekiq-cron \
	rubygem-redis-namespace>=1.5.2:databases/rubygem-redis-namespace \
	rubygem-httparty>=0.13.3:www/rubygem-httparty \
	rubygem-rainbow>=2.1.0:devel/rubygem-rainbow \
	rubygem-settingslogic>=2.0.9:devel/rubygem-settingslogic \
	rubygem-version_sorter>=2.1.0:textproc/rubygem-version_sorter \
	rubygem-redis-rails>=4.0.0:www/rubygem-redis-rails \
	rubygem-redis>=3.2:databases/rubygem-redis \
	rubygem-connection_pool>=2.0:net/rubygem-connection_pool \
	rubygem-hipchat>=1.5.0:net-im/rubygem-hipchat \
	rubygem-gitlab-flowdock-git-hook>=1.0.1:www/rubygem-gitlab-flowdock-git-hook \
	rubygem-gemnasium-gitlab-service>=0.2:devel/rubygem-gemnasium-gitlab-service \
	rubygem-slack-notifier>=1.2.0:devel/rubygem-slack-notifier \
	rubygem-asana>=0.4.0:www/rubygem-asana \
	rubygem-ruby-fogbugz>=0.2.1:devel/rubygem-ruby-fogbugz \
	rubygem-d3_rails-rails4>=3.5.0:www/rubygem-d3_rails-rails4 \
	rubygem-underscore-rails>=1.8.0:www/rubygem-underscore-rails \
	rubygem-sanitize>=2.0:textproc/rubygem-sanitize \
	rubygem-babosa>=1.0.2:textproc/rubygem-babosa \
	rubygem-loofah>=2.0.3:textproc/rubygem-loofah \
	rubygem-licensee>=8.0:devel/rubygem-licensee \
	rubygem-rack-attack>=4.3.1:www/rubygem-rack-attack \
	rubygem-ace-rails-ap>=4.1.0:www/rubygem-ace-rails-ap \
	rubygem-mousetrap-rails>=1.4.6:www/rubygem-mousetrap-rails \
	rubygem-charlock_holmes>=0.7.3:textproc/rubygem-charlock_holmes \
	rubygem-chronic>=0.10.2:devel/rubygem-chronic \
	rubygem-chronic_duration>=0.10.6:devel/rubygem-chronic_duration \
	rubygem-sass-rails5>=5.0.0:textproc/rubygem-sass-rails5 \
	rubygem-coffee-rails4>=4.1.0:devel/rubygem-coffee-rails4 \
	rubygem-uglifier>=2.7.2:www/rubygem-uglifier \
	rubygem-turbolinks-classic>=2.5.0:www/rubygem-turbolinks-classic \
	rubygem-jquery-turbolinks>=2.1.0:www/rubygem-jquery-turbolinks \
	rubygem-addressable>=2.3.8:www/rubygem-addressable \
	rubygem-bootstrap-sass>=3.3.0:www/rubygem-bootstrap-sass \
	rubygem-font-awesome-rails-rails4>=4.6.1:devel/rubygem-font-awesome-rails-rails4 \
	rubygem-gemojione>=3:graphics/rubygem-gemojione \
	rubygem-gon>=6.1.0:www/rubygem-gon \
	rubygem-jquery-atwho-rails-rails4>=1.3.2:www/rubygem-jquery-atwho-rails-rails4 \
	rubygem-jquery-rails4>=4.1.0:www/rubygem-jquery-rails4 \
	rubygem-jquery-ui-rails-rails4>=5.0.0:www/rubygem-jquery-ui-rails-rails4 \
	rubygem-request_store>=1.3.0:devel/rubygem-request_store \
	rubygem-select2-rails>=3.5.9:www/rubygem-select2-rails \
	rubygem-virtus>=1.0.1:devel/rubygem-virtus \
	rubygem-net-ssh>=3.0.1:security/rubygem-net-ssh \
	rubygem-base32>=0.3.2:converters/rubygem-base32 \
	rubygem-sentry-raven>=2.0.0:devel/rubygem-sentry-raven \
	rubygem-premailer-rails>=1.9.0:mail/rubygem-premailer-rails \
	rubygem-gitlab_meta>=7.0:devel/rubygem-gitlab_meta \
	rubygem-newrelic-grape>=0:devel/rubygem-newrelic-grape \
	rubygem-newrelic_rpm>=3.16:devel/rubygem-newrelic_rpm \
	rubygem-octokit>=4.3.0:net/rubygem-octokit \
	rubygem-mail_room>=0.8:mail/rubygem-mail_room \
	rubygem-email_reply_parser>=0.5.8:mail/rubygem-email_reply_parser \
	rubygem-ruby-prof>=0.15.9:devel/rubygem-ruby-prof \
	rubygem-activerecord-deprecated_finders>=1.0.3:devel/rubygem-activerecord-deprecated_finders \
	rubygem-activerecord-session_store>=1.0.0:databases/rubygem-activerecord-session_store \
	rubygem-nested_form>=0.3.2:www/rubygem-nested_form \
	rubygem-oauth2>=1.2.0:net/rubygem-oauth2 \
	rubygem-paranoia>=2.0:databases/rubygem-paranoia \
	rubygem-health_check>=2.1.0:devel/rubygem-health_check \
	rubygem-vmstat>=2.2:sysutils/rubygem-vmstat \
	rubygem-sys-filesystem>=1.1.6:sysutils/rubygem-sys-filesystem \
	rubygem-rinku>=1.7.3:www/rubygem-rinku

USE=	pgsql=yes
WANT=	pgsql=9.1+

USE_RUBY=	yes

USE_RC_SUBR=	gitlab
USE_GITHUB=	yes
GH_ACCOUNT=	gitlabhq
GH_PROJECT=	gitlabhq

USERS=	git
GROUPS=	git

NO_ARCH=	yes
NO_BUILD=	yes

do-install:
	${FIND} ${WRKSRC} -name '*.orig' -delete
	${FIND} ${WRKSRC} -name '*.bak' -delete
	${FIND} ${WRKSRC} -name '*.gitkeep' -delete
	${FIND} ${WRKSRC} -name '*.gitignore' -delete
	${FIND} ${WRKSRC} -name "Gemfile.lock" -delete
	${MV} ${WRKSRC}/config/gitlab.yml.example ${WRKSRC}/config/gitlab.yml.sample
	${MV} ${WRKSRC}/config/unicorn.rb.example ${WRKSRC}/config/unicorn.rb.sample
	${MV} ${WRKSRC}/config/resque.yml.example ${WRKSRC}/config/resque.yml.sample
	${MV} ${WRKSRC}/config/secrets.yml.example ${WRKSRC}/config/secrets.yml.sample
	${MV} ${WRKSRC}/config/initializers/rack_attack.rb.example ${WRKSRC}/config/initializers/rack_attack.rb.sample
	${CP} ${WRKSRC}/config/database.yml.postgresql ${WRKSRC}/config/database.yml.sample
	${MKDIR} ${STAGEDIR}/home/git/repositories
	${MKDIR} ${STAGEDIR}${PREFIX}/www/${PORTNAME}/public/assets
	${MKDIR} ${STAGEDIR}${PREFIX}/www/${PORTNAME}/tmp/cache
	${MKDIR} ${STAGEDIR}${PREFIX}/www/${PORTNAME}/tmp/sessions
	(cd ${WRKSRC} && ${COPYTREE_SHARE} . ${STAGEDIR}${PREFIX}/www/${PORTNAME})

.include <bsd.port.mk>
