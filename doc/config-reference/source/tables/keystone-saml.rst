..
    Warning: Do not edit this file. It is automatically generated from the
    software project's code and your changes will be overwritten.

    The tool to generate this file lives in openstack-doc-tools repository.

    Please make any changes needed in the code, then run the
    autogenerate-config-doc tool from the openstack-doc-tools repository, or
    ask for help on the documentation mailing list, IRC channel or meeting.

.. _keystone-saml:

.. list-table:: Description of SAML configuration options
   :header-rows: 1
   :class: config-ref-table

   * - Configuration option = Default value
     - Description
   * - **[saml]**
     -
   * - ``assertion_expiration_time`` = ``3600``
     - (Integer) Determines the lifetime for any SAML assertions generated by keystone, using `NotOnOrAfter` attributes.
   * - ``xmlsec1_binary`` = ``xmlsec1``
     - (String) Name of, or absolute path to, the binary to be used for XML signing. Although only the XML Security Library (`xmlsec1`) is supported, it may have a non-standard name or path on your system. If keystone cannot find the binary itself, you may need to install the appropriate package, use this option to specify an absolute path, or adjust keystone's PATH environment variable.
   * - ``certfile`` = ``/etc/keystone/ssl/certs/signing_cert.pem``
     - (String) Absolute path to the public certificate file to use for SAML signing. The value cannot contain a comma (`,`).
   * - ``keyfile`` = ``/etc/keystone/ssl/private/signing_key.pem``
     - (String) Absolute path to the private key file to use for SAML signing. The value cannot contain a comma (`,`).
   * - ``idp_entity_id`` = ``None``
     - (URI) This is the unique entity identifier of the identity provider (keystone) to use when generating SAML assertions. This value is required to generate identity provider metadata and must be a URI (a URL is recommended). For example: `https://keystone.example.com/v3/OS-FEDERATION/saml2/idp`.
   * - ``idp_sso_endpoint`` = ``None``
     - (URI) This is the single sign-on (SSO) service location of the identity provider which accepts HTTP POST requests. A value is required to generate identity provider metadata. For example: `https://keystone.example.com/v3/OS-FEDERATION/saml2/sso`.
   * - ``idp_lang`` = ``en``
     - (String) This is the language used by the identity provider's organization.
   * - ``idp_organization_name`` = ``SAML Identity Provider``
     - (String) This is the name of the identity provider's organization.
   * - ``idp_organization_display_name`` = ``OpenStack SAML Identity Provider``
     - (String) This is the name of the identity provider's organization to be displayed.
   * - ``idp_organization_url`` = ``https://example.com/``
     - (URI) This is the URL of the identity provider's organization. The URL referenced here should be useful to humans.
   * - ``idp_contact_company`` = ``Example, Inc.``
     - (String) This is the company name of the identity provider's contact person.
   * - ``idp_contact_name`` = ``SAML Identity Provider Support``
     - (String) This is the given name of the identity provider's contact person.
   * - ``idp_contact_surname`` = ``Support``
     - (String) This is the surname of the identity provider's contact person.
   * - ``idp_contact_email`` = ``support@example.com``
     - (String) This is the email address of the identity provider's contact person.
   * - ``idp_contact_telephone`` = ``+1 800 555 0100``
     - (String) This is the telephone number of the identity provider's contact person.
   * - ``idp_contact_type`` = ``other``
     - (String) This is the type of contact that best describes the identity provider's contact person.
   * - ``idp_metadata_path`` = ``/etc/keystone/saml2_idp_metadata.xml``
     - (String) Absolute path to the identity provider metadata file. This file should be generated with the `keystone-manage saml_idp_metadata` command. There is typically no reason to change this value.
   * - ``relay_state_prefix`` = ``ss:mem:``
     - (String) The prefix of the RelayState SAML attribute to use when generating enhanced client and proxy (ECP) assertions. In a typical deployment, there is no reason to change this value.
